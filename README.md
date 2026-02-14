# Python Port Scanner

A network port scanner written in Python, inspired by Nmap. Scans target hosts to identify open ports.

## Features

- Scans specified port ranges on target hosts
- Multi-threaded scanning for improved speed (if applicable)
- Displays open ports with their service names
- Simple command-line interface

## Prerequisites

- Python 3.x
- No external dependencies (or list any libraries you use)

## Installation
```bash
git clone https://github.com/yourusername/port-scanner.git
cd port-scanner
```

## Usage
```bash
python port_scanner.py <target_ip> [options]
```

**Examples:**
```bash
# Scan common ports on localhost
python port_scanner.py 127.0.0.1

# Scan specific port range
python port_scanner.py 192.168.1.1 -p 1-1000

# Scan specific ports
python port_scanner.py example.com -p 80,443,8080
```

## Options

- `-p, --ports`: Specify port range (e.g., 1-1000) or specific ports (e.g., 80,443)
- `-t, --timeout`: Set connection timeout in seconds (default: 1)
- `-h, --help`: Display help message

## Example Output
```
Scanning target: 192.168.1.1
[+] Port 22 (SSH) - OPEN
[+] Port 80 (HTTP) - OPEN
[+] Port 443 (HTTPS) - OPEN

Scan completed in 12.34 seconds
```

## How It Works

Brief explanation of your implementation:
- Uses Python's socket library to attempt connections
- Multi-threading to scan multiple ports simultaneously (if applicable)
- Timeout mechanism to avoid hanging on closed ports

## Limitations

- Basic TCP connect scan only (no SYN/stealth scanning)
- May be slower than professional tools like Nmap
- Requires appropriate network permissions

## Legal Disclaimer

⚠️ **Important:** Only scan networks and systems you own or have explicit permission to test. Unauthorized port scanning may be illegal in your jurisdiction.

## What I Learned

- Socket programming in Python
- Multi-threading and concurrent operations
- Network protocols and port concepts
- Error handling for network operations

## Future Improvements

- [ ] Add UDP scanning support
- [ ] Implement service version detection
- [ ] Add output to file option
- [ ] Create GUI interface

## Contributing

This is a learning project, but suggestions and improvements are welcome! Feel free to open an issue or submit a pull request.

## License

MIT License (or whatever license you choose)

## Acknowledgments

- Inspired by Nmap
- Built as a learning project to understand network scanning
