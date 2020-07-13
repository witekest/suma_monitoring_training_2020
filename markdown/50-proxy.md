<!-- .slide: data-state="divider" id="proxy-cover" data-timing="20s" data-menu-title="Reverse Proxy" -->
# Exporters Reverse Proxy (preview)


<!-- .slide: data-state="normal" id="firewall" data-timing="20s" data-menu-title="Minions Behind Firewall" -->
## Monitored Minion Behind Firewall

<div class="breadcrumbs">Reverse Proxy</div>

* each monitored **target** has to be reachable over HTTP
* problematic for security and maintenance

<!-- .element class="col1" -->

![Firewall](images/firewall.png)

<!-- .element class="col2" -->


<!-- .slide: data-state="normal" id="proxy" data-timing="20s" data-menu-title="Proxy Mapping" -->
## Reverse Proxy for Exporters

<div class="breadcrumbs">Reverse Proxy</div>

* install **_Exporter Exporter_** on each minion behind proxy
* **single port** can be used to query **multiple exporters**
* much simpler firewall configuration
* supported in Uyuni service discovery


<!-- .slide: data-state="normal" class="full-screen" id="proxy-formula" data-timing="20s" data-menu-title="Exporters Formula" -->
<img src="images/exporters_formula.png">


<!-- .slide: data-state="normal" id="proxy-formula-2" data-timing="20s" data-menu-title="Exporters Formula" -->
## Formula for Proxied Exporters

<div class="breadcrumbs">Reverse Proxy</div>

* **_Arguments_** has higher precedence than **_Address_**
* empty **hostname** indicates localhost


<!-- .slide: data-state="normal" id="proxy-configuration" data-timing="20s" data-menu-title="Proxy Configuration" -->
## Proxy Configuration

<div class="breadcrumbs">Reverse Proxy</div>

```yaml
==> apache.yaml <==
method: http
http:
   port: 9117

==> node.yaml <==
method: http
http:
   port: 9100

==> postgres.yaml <==
method: http
http:
   port: 9187
```

```
GET http://minion:9100/metrics		→	GET http://minion:9999/proxy?module=node
```
