<!-- .slide: data-state="divider" id="divider-no-image" data-timing="20s" data-menu-title="Introduction on Prometheus and Grafana" -->
# Introduction on Prometheus and Grafana


<!-- .slide: data-state="normal" id="" data-timing="20s" data-menu-title="What is Monitoring" -->
## What is Monitoring?

<div class="breadcrumbs">Introduction on Prometheus and Grafana</div>

*   **Collect** system and application metrics / measurements
*   **Evaluate** them; calculate meaningful data
*   **Store** them; e.g. in time series database
*   **Visualise** them; for humans
*   **Alert**


<!-- .slide: data-state="normal" id="" data-timing="20s" data-menu-title="Why Monitoring" -->
## Why is Monitoring useful?

<div class="breadcrumbs">Introduction on Prometheus and Grafana</div>

*   **Improve system / application uptime**
    * avoid failures proactively
*   **Reduce administration burden**
    * help in _ad hoc_ failure retrospective
*   **Resource optimization**
    * analyze long-term trends
*   **Prevent bottlenecks**
    * avoid service degradation


<!-- .slide: data-state="normal" id="prometheus" data-timing="20s" data-menu-title="Prometheus" -->
## Prometheus

<div class="breadcrumbs">Introduction on Prometheus and Grafana</div>

* **_state of the art_** monitoring tool
* built-in time series database
* implements **_PULL_** model
* centrally managed configuration
* measurements collected from **_instrumented applications_**

  or exposed by **_exporters_**
* flexible query language

<!-- .element class="col1-large" -->

![Image in column two](images/Prometheus_software_logo.svg)

<!-- .element class="col2-small" -->


<!-- .slide: data-state="normal" id="grafana" data-timing="20s" data-menu-title="Grafana" -->
## Grafana

<div class="breadcrumbs">Introduction on Prometheus and Grafana</div>

* interactive tool for **_data visualisation_**
* supports multiple datasources
* customizable and pluggable

<!-- .element class="col1-large" -->

![Image in column two](images/Grafana_logo.svg)

<!-- .element class="col2-small" -->


  <!-- .slide: data-state="normal" id="grafana" data-timing="20s" data-menu-title="SUMA monitoring" -->
  ## Monitoring with SUSE Manager

  <div class="breadcrumbs">Introduction on Prometheus and Grafana</div>

  <img src="images/suma_monitoring.svg" width="750">
