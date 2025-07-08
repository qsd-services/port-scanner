# Port Scanner

A simple yet powerful command-line TCP port scanner written in Go. This tool allows you to scan a target host for open ports within a specified range, with configurable concurrency.

## Features

*   **Host Scanning:** Scan any IP address or hostname.
*   **Custom Port Range:** Define the starting and ending ports for your scan.
*   **Concurrency Control:** Adjust the number of concurrent connections for faster scanning.
*   **Clear Output:** Displays all open ports found within the scanned range.

## Installation

To build and install the port scanner, ensure you have Go (version 1.24.4 or higher) installed on your system.

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/your-username/port-scanner.git # Replace with your actual repo URL
    cd port-scanner
    ```
2.  **Build the executable:**
    ```bash
    go build -o port-scanner
    ```
    This will create an executable named `port-scanner` in the current directory.

## Usage

Run the `port-scanner` executable with the desired flags.

```bash
./port-scanner [flags]
```

### Flags:

*   `-host <hostname_or_ip>`: Specifies the target host to scan (default: `localhost`).
*   `-start <port_number>`: Sets the starting port for the scan (default: `1`).
*   `-end <port_number>`: Sets the ending port for the scan (default: `1024`).
*   `-c <number_of_goroutines>`: Defines the number of concurrent goroutines (connections) to use during the scan (default: `100`).

### Examples:

1.  **Scan localhost for common ports (1-1024):**
    ```bash
    ./port-scanner
    ```

2.  **Scan a specific IP address for a custom range:**
    ```bash
    ./port-scanner -host 192.168.1.1 -start 8000 -end 9000
    ```

3.  **Scan a hostname with increased concurrency:**
    ```bash
    ./port-scanner -host example.com -c 200
    ```

4.  **Scan a specific port:**
    ```bash
    ./port-scanner -host 127.0.0.1 -start 22 -end 22
    ```

## License

This project is licensed under the Apache License 2.0 - see the [LICENSE](LICENSE) file for details.

## Contributing

Contributions are welcome! Please feel free to open issues or submit pull requests.
