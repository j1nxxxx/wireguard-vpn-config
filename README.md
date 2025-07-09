# WireGuard VPN (Self-Hosted) + Remote Access

This project documents the setup of a self-hosted WireGuard VPN server to securely access services in a Linux-based home lab environment.

**WireGuard**: Fast, modern VPN protocol with strong encryption  
**Use Cases**: Secure remote access to internal services such as SMB and SSH

## Tech Stack

- Operating System: Debian Linux  
- WireGuard VPN  
- Bash Shell Scripting  
- `iptables` Firewall

## Features

- Lightweight VPN server using WireGuard  
- Key-based peer authentication  
- NAT routing and DNS leak protection  
- Cross-platform support: Linux, Windows, Android  

## Use Cases

- Remote access to **SMB server** without exposing ports publicly  
- Secure SSH management of home server from external networks  
- Encrypted tunnelling for all traffic when on untrusted networks  

## Network Security

- WireGuard runs on a **non-standard port** to reduce automated scans  
- Firewall configured to **allow VPN traffic only from known peers**  
- Internal services like SSH and SMB are **not publicly exposed**, accessible only through the VPN  
- DNS requests routed through the VPN to prevent leaks  

## Protocol & Access Control

- Only strong, modern encryption via WireGuard (ChaCha20 + Poly1305)  
- SSH hardened with key-based login
- SMB access restricted by subnet and user authentication  
- Guest/anonymous access fully disabled on all internal services
