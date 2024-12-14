# KeyDjiin-kit

<h1 align="center">
  <br>
  <a href="https://github.com/KeyDjiin-kit"><img  alt="Photon"></a>
  <br>
  KeyDjiin-kit
  <br>
</h1>

<h4 align="center">Reconnaissance Swiss Army Knife</h4>

<p align="center">
  <a href="https://github.com/KeyDjiin/releases">
    <img src="https://img.shields.io/github/release/KeyDjiin.svg">
  </a>
  <a href="https://github.com/KeyDjiin-kit">

 </a>
  <a href="https://github.com/KeyDjiin/issues?q=is%3Aissue+is%3Aclosed">
      <img src="https://img.shields.io/github/issues-closed-raw/KeyDjiin/KeyDjiin.svg">
  </a>
</p>

### Main Features
- Wizard + CLA interface
- Can extracts targets from STDIN (piped input) and act upon them
- All the information is extracted with APIs, no direct contact is made to the target


### Utilities
- [Censys](https://censys.io/): Uses censys.io to gather massive amount of information about an IP address.
- [NS Lookup](https://hackertarget.com/dns-lookup/): Does name server lookup
- [Port Scan](https://hackertarget.com/tcp-port-scan/): Scan most common TCP ports
- [Detect CMS](https://whatcms.org): Can detect 400+ content management systems
- [Whois lookup](https://hackertarget.com/whois-lookup/): Performs a whois lookup
- [Detect honeypot](https://honeyscore.shodan.io/): Uses shodan.io to check if target is a honeypot
- [Find subdomains](https://findsubdomains.com): Uses findsubdomains.com to find subdomains
- [Reverse IP lookup](https://hackertarget.com/reverse-ip-lookup/): Does a reverse IP lookup to find domains associated with an IP address
- [Detect technologies](https://www.wappalyzer.com): Uses wappalyzer.com to detect 1000+ technologies
- [All](https://github.com/s0md3v/ReconDog): Runs all utilities against the target

### Demo
<a href="https://youtu.be/CHkIMcSzzCY"><img alt="demo" src="https://image.ibb.co/i11A69/Screenshot-2018-10-13-15-41-11.png"></a>

### Compatibility
Recon Dog will run on anything that has a python interpreter installed. However, it has been tested on the following configurations:

Operating Systems: Windows, Linux, Mac\
Python Versions: Python2.7, Python 3.6

### Installation
KeyDjiin kit requires no manual configuration and can be simply run as a normal python script.\
However, a debian package can be downloaded from [here](https://github.com/KeyDjiin/KeyDjiin-kitraw=true) if you want to install it.

### Usage
#### Wizard Interface
Wizard interface is the most straightforward way you can use KeyDjiin-kit in. Just run the program, select what you want to do and enter the target, it's that simple.
#### CLA Interface
KeyDjiin also has a **C**ommand **L**ine **A**rgument inteface.
Here's how you can find subdomains:

`python dog -t marvel.com -c 7`

There's more to it! Do you have a program that can enumerate subdomains and you want to scan ports of all the subdomains it finds? Don't worry, KeyDjiin toolkit is designed for handling with such cases. You can simply do this:

`subdomainfinder -t example.com | python dog --domains -c 3`

If you just want to print the targets, don't use the **-c** option.\
Also, it doesn't matter what kind of output the other program generates, Recon Dog uses regular expressions to find targets which makes it easy to integrate will literally every tool.
There are two switchs available:
```
--domains    extract domains from STDIN
--ips        extract ip addresses from STDIN
```

### Contribution & License
You can contribute in following ways:

- Report bugs
- Develop plugins
- Give suggestions to make it better
- Fix issues & submit a pull request

Do you want to have a conversation in private? Hit me up on [my twitter](https://twitter.com/Xxxe556), inbox is open :) \
KeyDjiin toolkit is licensed under **Apache 2.0 License**.
