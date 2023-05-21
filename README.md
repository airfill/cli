![image](https://airfill.io/afgit15.png)
## CLIs for airfill 5G RAN

airfill's powerful status and configuration command-line interfaces (CLIs) provide comprehensive control over the 5G RAN platform. To ensure seamless deployment and ease of use, CLIs are deployed using Docker, offering enhanced portability across various environments.

The CLIs feature an intuitive command structure and provide clear and informative outputs, enabling users to easily interact with the system, monitor its status, and configure its settings.

For continuous monitoring and extensive key performance indicators (KPIs) [airfill AFI](https://github.com/airfill/afi) containers can be deployed.

### Install Docker
If you do not have Docker Engine installed, please follow official Docker [installation guide](https://docs.docker.com/engine/install/ubuntu/).

### Status CLI

Get the latest version from Docker hub:
```
$ sudo docker pull airfill/afcli_gnb_status:latest
```
Use 'cell_info' command to get overall status of the RAN
```
$ sudo docker run airfill/afcli_gnb_status --ip <bu_ip_addr> --cmd cell_info
```
For other available commands:
```
$ sudo docker run airfill/afcli_gnb_status --help
```

### Configuration CLI

Get the latest version from Docker hub:
```
$ sudo docker pull airfill/afcli_gnb_config:latest
```
You can use commands like:
```
$ sudo docker run airfill/afcli_gnb_config --ip <bu_ip_addr> --cmd set_5gc_ip <5gc_ip_addr>
```
For available commands:
```
$ sudo docker run airfill/afcli_gnb_config --help
```
