# Awesome-Web-Application-Firewall-WAF

## Top Web Application Firewall (WAF) Ecosystem



**Curated List of SaaS Products & Open-Source GitHub Projects**

*Focused on Application-Layer Attack Defense, API Protection & Self-Hosted WAF Engines*

**Last updated: October 2026**



This repository tracks notable **commercial WAF platforms** and **open-source projects** that protect web applications and APIs from attacks like SQL injection, cross-site scripting (XSS), and zero-day exploits. These tools inspect HTTP/HTTPS traffic at Layer 7, blocking malicious requests before they reach your origin servers.



**Examples** include AWS WAF, Cloudflare WAF, Akamai App & API Protector, Fastly Next-Gen WAF, Imperva Cloud WAF, F5 Distributed Cloud WAF, Azure WAF, Fortinet FortiWeb Cloud, Radware Cloud WAF, and Palo Alto Cloud WAF (the category leaders).



**Open-source emphasis**: WAF is a strong open-source domain. **ModSecurity** remains the most widely deployed WAF engine with over 10,000 deployments . **OWASP Coraza** is the modern Go-based alternative, fully compatible with CRS v4 . **SafeLine** leads with 400,000+ installations and 1M+ protected websites . **BunkerWeb** provides a cloud-native, sovereign WAAP solution . This section is heavily expanded.



Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.



## Table of Contents

- [SaaS/Hosted Platforms](#saas-hosted-platforms)

- [Open-Source GitHub Projects](#open-source-github-projects)

- [How to Contribute](#how-to-contribute)

- [Disclaimer](#disclaimer)



## SaaS/Hosted Platforms



- **[Cloudflare WAF](https://www.cloudflare.com/waf/)**  

  Cloud-edge WAF with managed rulesets updated automatically, custom rules via Cloudflare Rules Language, and real-time Security Analytics. **Included in paid plans with limited free tier** .



- **[AWS WAF](https://aws.amazon.com/waf/)**  

  Native AWS WAF integrated with CloudFront, ALB, API Gateway, and AppSync. Supports managed rules, rate-based rules, and Web ACLs for policy standardization. **Paid per rule + per million requests** .



- **[Akamai App & API Protector](https://www.akamai.com/)**  

  Enterprise WAF with adaptive intelligence, API protection, and bot management.



- **[Fastly Next-Gen WAF](https://www.fastly.com/)**  

  Signal Sciences-based WAF with real-time visibility and blocking.



- **[Imperva Cloud WAF](https://www.imperva.com/)**  

  Enterprise cloud WAF with DDoS protection and API security.



- **[F5 Distributed Cloud WAF](https://www.f5.com/)**  

  SaaS-based WAF with bot defense and API protection.



- **[Azure WAF](https://azure.microsoft.com/en-us/products/web-application-firewall)**  

  Microsoft's WAF integrated with Azure Application Gateway and Front Door.



- **[Fortinet FortiWeb Cloud](https://www.fortinet.com/)**  

  Cloud WAF with ML-based anomaly detection and API protection.



- **[Radware Cloud WAF](https://www.radware.com/)**  

  Enterprise WAF with behavioral analysis and DDoS mitigation.



- **[Palo Alto Cloud WAF](https://www.paloaltonetworks.com/)**  

  Prisma Cloud WAF with integrated security posture management.



## Open-Source GitHub Projects



- **[ModSecurity](https://github.com/owasp-modsecurity/ModSecurity)**  

  **The most widely deployed open-source WAF engine**, Apache-2.0 licensed with 10,000+ deployments . **Runs as a module for Apache, Nginx, and IIS** — supports OWASP Core Rule Set (CRS) for OWASP Top 10 protection. **Trade-off**: Trustwave commercial support ended July 2024, but community maintenance continues with security patches . **Best for traditional Nginx/Apache stacks requiring proven WAF engine** .



- **[OWASP Coraza](https://github.com/corazawaf/coraza)**  

  **Modern open-source WAF written in Go**, Apache-2.0 licensed. **100% compatible with OWASP CRS v4** and ModSecurity SecLang rulesets. **20-40% higher throughput than ModSecurity** in benchmarks . **Integrations**: Caddy (stable), Envoy (stable), HAProxy (experimental), Nginx (experimental C library). **The go-to choice for Kubernetes/Envoy environments** .



- **[SafeLine](https://github.com/chaitin/SafeLine)**  

  **Self-hosted WAF with semantic engine detection**, GPL-3.0 licensed with **7,114+ GitHub stars** . **400,000+ installations worldwide, protecting 1M+ websites, handling 30B+ HTTP requests daily** . **Benchmark**: 71.65% detection rate (Balance mode) vs ModSecurity Level 1 at 69.74%, with **0.07% false positive rate** . Features anti-bot challenges, rate limiting, HTML/JS encryption. **Best for production-ready self-hosted WAF with strong detection and low false positives** .



- **[BunkerWeb](https://github.com/bunkerity/bunkerweb)**  

  **Cloud-native, sovereign WAF/WAAP**, AGPL-3.0 licensed with **96% quality rating** . **Runs as reverse proxy for Linux, Docker, and Kubernetes**. Features OWASP Top 10 protection, anti-bot, HTTPS management, OpenAPI validator, mTLS, geoblocking, and caching . **The best choice for EU sovereign deployments and Kubernetes-native environments** .



- **[Naxsi](https://github.com/nbs-system/naxsi)**  

  **Lightweight Nginx WAF module**, GPL-3.0 licensed. **Low deployment complexity** — ideal for resource-constrained environments . **Best for simple Nginx deployments needing basic protection** .



- **[OpenResty](https://github.com/openresty/openresty)**  

  **Nginx + LuaJIT platform for high-performance WAF**, BSD-2-Clause licensed. **lua-resty-waf module** enables custom rules and AI-driven anomaly detection . **50,000+ QPS single-machine performance** — best for high-concurrency scenarios .



- **[GuardianWAF](https://github.com/guardianwaf/guardianwaf)**  

  **Modern Go-based WAF with MCP server integration**, open-source . Features **21 MCP tools** for AI agent integration (Claude Code, Claude Desktop, VS Code), **<1ms p99 latency overhead**, Docker/Kubernetes deployment . **Best for AI-agent-managed WAF deployments** .



- **[Aegis](https://github.com/divinelabio/Aegis)**  

  **Next-gen self-hosted WAF & edge reverse proxy in Go**, open-source . Features **HTTP/3 (QUIC) support, auto SSL/TLS via Let's Encrypt, load balancing, geo-blocking, connection protection**, and centralized management console with 2FA . **Best for modern edge deployment with comprehensive features** .



### The Rule Engine: OWASP CRS



- **[OWASP Core Rule Set (CRS)](https://github.com/coreruleset/coreruleset)**  

  **The standard rule set for ModSecurity and Coraza**, Apache-2.0 licensed. **CRS v4.25.0 is the first LTS release** — stable foundation with extended security patches . **CRS v4.28.0** (July 2026) fixed **CVE-2026-21876** (CRITICAL CVSS 9.3, XML attribute bypass) and a ReDoS vulnerability . **CRS v4.29.0** (August 2026) added expanded web shell detection and evasion detection improvements . **Essential companion to any ModSecurity/Coraza deployment** .



- **[CRS Documentation & Benchmarks](https://coreruleset.org/)**  

  Official CRS project site with rule documentation, paranoia levels (PL1-PL4), anomaly scoring configuration, and performance guidance .



### Additional Strong Open-Source Options



- **WAF Comparison Project (openappsec)** — Open-source testing framework comparing WAF efficacy across vendors. Includes 1M+ legitimate requests and 73,924 malicious payloads for benchmarking .

- **purple-wolf** — Rust-based WAF with Traefik WASM plugin integration. Benchmarked at **2.4× more attack detection** than Coraza at same resource ceiling, with only 0.1-0.2ms p99 latency overhead .

- **modsecurity-crs-docker** — Official Docker images combining ModSecurity with OWASP CRS for quick deployment .

- **RuiQi WAF** — Web management panel and enhanced traffic control for Coraza SPOA .



**Frameworks for building custom WAF solutions**: Combine **OWASP CRS** as the rule engine foundation with **ModSecurity** for traditional Nginx/Apache stacks  or **Coraza** for modern Go/Kubernetes environments . Use **SafeLine** for production-ready self-hosted WAF with semantic detection and low false positives . Deploy **BunkerWeb** for cloud-native, sovereign WAF/WAAP with OWASP Top 10 and anti-bot protection . Choose **GuardianWAF** for AI-agent-managed WAF with MCP integration . Note that **high false positive rates (10-17.58%) with default CRS rules** require careful tuning — plan for log-only mode before production blocking .



## How to Contribute



1. Fork the repo.

2. Add/edit entries in `README.md` (follow existing format).

3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.

4. Submit PR with a short explanation.



Star the repo if you find it useful!



## Disclaimer



- This is a **community-curated** list — not exhaustive and not an endorsement.

- WAF platforms inspect all HTTP/HTTPS traffic and must be properly tuned. **False positives (10-17.58% with default CRS rules) can block legitimate users** — always test in log-only mode before enabling blocking .

- **Trustwave commercial support for ModSecurity ended July 2024** — community continues security patches (v3.0.15/3.0.16 in 2026), but no structured vendor support . **Coraza is the modern replacement** for new deployments .

- **Open-source WAF requires operational expertise** — rule tuning, CRS updates, and security patching are ongoing responsibilities. Without dedicated security resources, a managed WAF may be more appropriate .

- **CRS updates are critical** — CVE-2026-21876 (CRITICAL, XML attribute bypass) and ReDoS vulnerabilities were fixed in v4.28.0 . Monitor the official CRS blog for security releases .

- The open-source ecosystem provides strong WAF engines and rule sets, but **managed threat intelligence, zero-day protection, and vendor-supported SLAs** remain primarily commercial offerings.



---



**Made for security engineers, DevSecOps teams, and organizations seeking WAF sovereignty.**

Let's make web application security more open, transparent, and tunable.
