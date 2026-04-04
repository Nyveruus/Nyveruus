I'm an autodidact from Spain. I value depth of knowledge rather than simply knowing how to use ephemeral tools. Understanding the system is what makes you able to administer and defend it effectively.

Overall, I gravitate towards low-level programming because there are generally no abstractions to hide behind, and I find the elegance and precision of statically typed languages like C to be compelling. Broadly speaking, I'm learning about systems programming, socket programming, and Linux internals, with an eye towards system administration. My favourite languages are C and Bash. 

Most of my time goes into projects, books, and man pages (lots of man pages...)

**Languages:** C, Bash, Python, Javascript, HTML/CSS  
**Learning:** x86-64 ASM, Go

### Reading

- CS:APP
- OSTEP

## Notable Learning Projects in C

- [Keylogger](https://github.com/Nyveruus/security-research/tree/main/offensive-security/tools/keylogger) — Kernel-level keylogger that records a keyboard event file in /dev/input and then exfiltrates over TCP. It reads the stream into input_event structs (from linux/input.h) for parsing and recording. It includes detection and prevention in the README  
- [SYN Scanner](https://github.com/Nyveruus/systems-programming/tree/main/projects/networking/port-scanner) — TCP port scanner that never completes the handshake. It implements a detached thread for listening for SYN-ACKS and printing the open ports, while another thread is in charge of creating and dispatching SYN packets with a raw socket. The raw socket is necessary for never completing the handshake, and IP/TCP headers and along with their checksums must and are manually computed for the socket.
- [Packet Sniffer](https://github.com/Nyveruus/systems-programming/tree/main/projects/networking/packet-sniffer) — Promiscuous frame capture across all interfaces (or used specified), writes to a rolling 2hr .pcap file readable in tcpdump or Wireshark. It operates as a systemd service through install and uninstall Bash scripts. It catches all frames at the socket level after setting promisc mode with ioctl. Filtering occurs at a higher level with if_indextoname() and comparing to argv. A PCAP global header is written on each initialization of the PCAP file and PCAP packet headers are implemented after ever recv
- [HTTP Server](https://github.com/Nyveruus/systems-programming/tree/main/projects/networking/http-server) — HTTP/1.1 static file server with MIME support. Accept and then thread model. Uses TCP socket and parses HTTP GET methods with regex. If indicated file in GET returns a fd, then 200 ok is returned along with the file. If no file is found, then 404 is returned.
- [TCP Server & Client](https://github.com/Nyveruus/systems-programming/tree/main/projects/networking/tcp-suite) — Poll-based TCP chat, server broadcasts to all clients, handles up to 100 concurrent connections. Client connections and disconnections are tracked with poll 
- [IPC](https://github.com/Nyveruus/systems-programming/tree/main/projects/ipc) — Unix pipes, I/O redirection and parallel process execution using fork, dup2, execl...
- [Hexdump Tool](https://github.com/Nyveruus/systems-programming/tree/main/tools/hexdump) — xxd-style hex dump utility with configurable width, grouping, and column output with argument parsing with getopt(). For pipelines.  

## Notable Learning Projects in Bash

- [Linux Audit Tool](https://github.com/Nyveruus/Linux-and-bash/tree/main/security/audit-tool) — Linux auditing and hardening tool for Debian. Checks accounts, SSH config, password policy, and file permissions.
