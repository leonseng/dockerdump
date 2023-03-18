# dockerdump

`dockerdump` provides a simple way to capture packets on the interface of a Docker container using `tcpdump`.

## Usage
To use this script, simply run the following command:

```
dockerdump <container> [tcpdump-options]
```

Example:

```
# by container name
sudo dockerdump my_container -s 0 -w my_packets.pcap

# by container id
sudo dockerdump 392faad5b085 -nnv -s 0 -w my_packets_2.pcap
```

## Installation

To install this script, follow these steps:

1. Download the script using curl:
    ```
    curl -o- https://raw.githubusercontent.com/leonseng/dockerdump/main/dockerdump.sh | sudo tee /usr/local/bin/dockerdump >/dev/null
    ```
1. Make the script executable:
    ```
    sudo chmod +x /usr/local/bin/dockerdump
    ```
