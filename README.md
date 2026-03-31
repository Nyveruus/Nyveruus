I'm a self-taught systems programmer from Spain. I value depth, knowing how things truly work under the hood, rather than simply how to use them. Understanding the system is what makes you able to administer and defend it effectively.

I gravitate towards low-level programming because there are generally no abstractions to hide behind, and I find the elegance and precision of statically typed languages like C to be compelling. My focus is systems programming, \*nix internals, and networking. My favourite languages are C and Bash. 

Most of my time goes into projects, books, and man pages (lots of man pages...)

**Languages:** C, Bash, Python, Javascript, HTML/CSS  
**Learning:** x86-64 ASM, Go

### Reading

- CS:APP
- OSTEP

## Notable Projects in C

- [Keylogger](https://github.com/Nyveruus/security-research/tree/main/offensive-security/tools/keylogger) — Kernel-level keylogger that reads raw /dev/input events, exfiltrating over TCP. It includes detection and prevention notes  
- [Packet Sniffer](https://github.com/Nyveruus/systems-programming/tree/main/projects/networking/packet-sniffer) — Promiscuous frame capture across all interfaces, writes to a rolling 2hr .pcap file. Systemd service.  
- [SYN Scanner](https://github.com/Nyveruus/systems-programming/tree/main/projects/networking/port-scanner) — Builds IP/TCP headers from scratch, checksums are manually computed. Multithreaded SYN scan, no full handshake.  
- [HTTP Server](https://github.com/Nyveruus/systems-programming/tree/main/projects/networking/http-server) — HTTP/1.1 static file server, accept-then-thread model, MIME type support. No libraries.  
- [TCP Server & Client](https://github.com/Nyveruus/systems-programming/tree/main/projects/networking/tcp-suite) — Poll-based TCP chat, server broadcasts to all clients, handles up to 100 concurrent connections.  
- [IPC](https://github.com/Nyveruus/systems-programming/tree/main/projects/ipc) — Unix pipes, I/O redirection and parallel process execution from scratch using fork, dup2, execl.  
- [Hexdump Tool](https://github.com/Nyveruus/systems-programming/tree/main/tools/hexdump) — xxd-style hex dump utility with configurable width, grouping, and column output with proper argument parsing with getopt(). Built for pipelines.  

## Notable Projects in Bash

- [Linux Audit Tool](https://github.com/Nyveruus/Linux-and-bash/tree/main/security/audit-tool) — Linux auditing and hardening tool for Debian. Checks accounts, SSH config, password policy, and file permissions.
