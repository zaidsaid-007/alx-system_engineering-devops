# Load Balancer

In this project, I expanded the configuration of the web server set up in project 0x0B. Two additional servers were issued: one to replicate the Nginx configuration of the original server, and another to set up an HAproxy load balancer to manage both web servers.

## Tasks :page_with_curl:

* **0. Double the number of webservers**
  * [0-custom_http_response_header](./0-custom_http_response-header): This Bash script installs and configures Nginx on a server with a custom HTTP response header.
    * The custom HTTP header is named `X-Served-By`.
    * The value of the HTTP header is the hostname of the server.

* **1. Install your load balancer**
  * [1-install_load_balancer](./1-install_load_balancer): This Bash script installs and configures HAproxy version 1.5 on a server.
    * It enables management via the init script.
    * Requests are distributed using a round-robin algorithm, ensuring efficient load balancing across the web servers.
