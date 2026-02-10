# AWS Static Website Hosting & Secure Delivery

## Project Overview

This project documents the design and deployment of a personal portfolio website using AWS managed services. The focus of the implementation is secure public delivery, operational reliability, and cost-aware infrastructure rather than frontend design alone.

The website is hosted as a static application and delivered globally over HTTPS using AWS-native services.

---

## Problem Statement

Personal websites are often hosted using shared hosting platforms with limited visibility into security controls, logging, or delivery mechanisms. These approaches provide minimal insight into how web traffic is handled and do not reflect real-world infrastructure practices.

This project addresses that gap by implementing a production-style static website architecture that emphasizes:
- Secure delivery
- High availability
- Minimal operational overhead
- Clear separation of responsibilities between services

---

## Architecture Summary

The solution uses the following AWS services:

- **Amazon S3**
  - Stores static website assets (HTML, CSS, JavaScript)
  - Configured with blocked public access
  - Access restricted to CloudFront only

- **Amazon CloudFront**
  - Acts as the public-facing content delivery network (CDN)
  - Enforces HTTPS
  - Provides low-latency global access

- **AWS Certificate Manager (ACM)**
  - Issues and manages the SSL/TLS certificate
  - Enables encrypted HTTPS connections

- **Domain & DNS**
  - Custom domain configured via DNS
  - DNS records route traffic to CloudFront

---

## Security Considerations

- S3 buckets are not publicly accessible
- All traffic is served over HTTPS
- CloudFront acts as the only entry point to the website
- AWS managed certificates eliminate manual key handling
- IAM permissions follow least-privilege principles

---

## Operational Characteristics

- Fully serverless architecture
- No compute instances to manage
- Minimal ongoing maintenance
- Scales automatically with traffic
- Extremely low cost under typical usage

---

## Outcome

The result is a publicly accessible personal website delivered using a secure, scalable, and production-aligned cloud architecture. This project demonstrates practical knowledge of AWS hosting, content delivery, and security fundamentals rather than simple static site deployment.

---

## Key Skills Demonstrated

- AWS S3 static hosting
- CloudFront configuration
- HTTPS and certificate management
- DNS configuration
- Secure public access design
- Cost-aware cloud architecture
