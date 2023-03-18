# dockerdump

`dockerdump` makes it easy to capture packets on the interface of a Docker container using `tcpdump`.

## Usage
To use this script, simply run the following command:

```
dockerdump <container> [tcpdump-options]
```

Examples:

```
# by container name
sudo dockerdump my_container -s 0 host 10.0.0.1

# by container id
sudo dockerdump 392faad5b085 -nnv -s 0 port 443 -w my_packets.pcap
```

## Installation

To install this script, follow these steps:

1. Download the script using curl:
    ```
    curl -o- https://raw.githubusercontent.com/leonseng/dockerdump/main/dockerdump | sudo tee /usr/local/bin/dockerdump >/dev/null
    ```
1. Make the script executable:
    ```
    sudo chmod +x /usr/local/bin/dockerdump
    ```
