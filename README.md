# 🧪 Home Lab Setup for Penetration Testing

Virtual penetration testing lab with **Kali Linux** (attacker) and **Metasploitable 2** (vulnerable target).

## 🛠️ Tools Used
- VirtualBox (6.1+)
- Kali Linux 2025.1
- Metasploitable 2
- Nmap, Burp Suite, Metasploit

## 📁 Lab Architecture

Kali Linux] <-- NAT Network --> [Metasploitable 2]
192.168.100.4 192.168.100.5


## 🚀 Steps to Reproduce
1. Install VirtualBox
2. Download Kali ISO and Metasploitable VM
3. Create two VMs with `NAT Network` adapter
4. Start both VMs, find IPs using `ip a` (Kali) and `ifconfig` (Metasploitable)
5. Test connectivity: `ping 192.168.100.5` from Kali

## 📊 Sample Scan (Nmap)
```bash
nmap -sV -p- 192.168.100.5
