# Software Requirements Specification (SRS)

## Padayon-Fi: Smart WiFi Vendo with Dynamic Advertising Platform and Centralized Management

---

## 1. Introduction

### 1.1 Purpose
This Software Requirements Specification (SRS) document specifies the functional and non-functional requirements for the Padayon-Fi system in accordance with ISO 29148:2018 standards. This document serves as the contractual basis for system development and acceptance testing.

### 1.2 Scope

**Product Name:** Padayon-Fi Smart WiFi Vendo System

**Product Mission:**  
To provide a comprehensive, automated digital services kiosk that delivers WiFi access, financial services, and advertising capabilities while enabling centralized management for business operators.

**Key Benefits:**
- Automated revenue generation through multiple service channels
- Enhanced customer experience with modern payment options
- Centralized monitoring and management capabilities
- Dynamic advertising platform for additional revenue streams

**Major Functions:**
- WiFi access provisioning with session management
- Multi-modal payment processing (digital and physical)
- Mobile services (load top-up, e-wallet transactions)
- Utility bill payment processing
- Gaming credits distribution
- Customer loyalty program management
- Dynamic advertising content management
- Centralized remote monitoring and configuration

### 1.3 Product Overview

#### 1.3.1 Product Perspective
Padayon-Fi is a new, self-contained product consisting of:
- **Hardware Component:** Physical kiosk with embedded computing system
- **Embedded Software:** Real-time kiosk operation system
- **Cloud Backend:** Distributed services for data management and processing
- **Management Interface:** Web-based administrative dashboard
- **Integration Layer:** APIs for third-party service providers

#### 1.3.2 Product Position
This system replaces traditional coin-only WiFi vendo machines with a modern, feature-rich alternative targeting the Philippine market's evolving digital payment preferences.

### 1.4 Definitions, Acronyms, and Abbreviations

| Term     | Definition |
|----------|------------|
| API      | Application Programming Interface |
| e-loading| Electronic mobile phone credit top-up service |
| GCash    | Philippine mobile wallet and online payment platform |
| IoT      | Internet of Things |
| Maya     | Philippine digital wallet platform (formerly PayMaya) |
| NFC      | Near Field Communication |
| QR       | Quick Response (code) |
| SLA      | Service Level Agreement |
| SMS      | Short Message Service |
| SSL/TLS  | Secure Sockets Layer/Transport Layer Security |
| UI       | User Interface |
| UX       | User Experience |
| Vendo    | Vending machine (Filipino colloquial term) |

### 1.5 References
- ISO 29148:2018 - Systems and software engineering - Life cycle processes - Requirements engineering
- ISO/IEC 25010:2011 - Software product Quality model
- PCI DSS - Payment Card Industry Data Security Standard
- BSP Circular No. 1049 - Guidelines on Electronic Money (E-Money)
- Republic Act No. 10173 - Data Privacy Act of 2012

### 1.6 Document Organization
This SRS follows the organization recommended by ISO 29148:
- Section 1: Introduction and scope
- Section 2: Overall description and context
- Section 3: Specific requirements (functional and non-functional)
- Section 4: Verification and acceptance criteria
- Section 5: Supporting information

---

## 2. Overall Description

### 2.1 Product Context

#### 2.1.1 System Context
The Padayon-Fi system operates within the Philippine digital services ecosystem, interfacing with:
- **Financial Service Providers:** GCash, Maya, banking networks
- **Telecommunications Operators:** Smart, Globe, DITO for mobile services
- **Utility Companies:** Meralco, Manila Water, etc., for bill payments
- **Gaming Platforms:** Mobile Legends, Valorant, Roblox for credits
- **Internet Infrastructure:** Local ISPs and network providers

#### 2.1.2 System Interfaces
- **User Interface:** Touch screen kiosk interface
- **Payment Interfaces:** Coin acceptor, NFC readers, QR scanners
- **Network Interface:** WiFi router integration and internet connectivity
- **Management Interface:** Web-based administrative dashboard
- **External APIs:** Third-party service provider integrations

### 2.2 Product Functions Summary

#### 2.2.1 Primary Functions
- **F1. WiFi Access Provisioning:** Time-based internet access, concurrent sessions, bandwidth control.
- **F2. Payment Processing:** Coins, GCash, Maya; payment validation; refunds.
- **F3. Additional Services Delivery:** Mobile load, e-wallet cash-in, bills payment, gaming credits.
- **F4. Customer Management:** Loyalty program, transaction history, promotions.
- **F5. Advertising Management:** Dynamic ads, scheduling, analytics.
- **F6. System Management:** Remote monitoring, analytics, maintenance alerts

### 2.3 User Characteristics
- **End Customers:** Age 15–65, basic tech skills, smartphone users.
- **Business Operators:** Basic business skills, daily monitoring, revenue tracking.
- **System Administrators:** Advanced technical skills, troubleshooting, remote maintenance.

### 2.4 Limitations and Constraints
- **Regulatory:** BSP compliance, Data Privacy Act, business permits.
- **Technical:** Embedded system limits, API rate limits, network dependency.
- **Business:** Hardware cost limits, provider partnerships, market-specific needs.

### 2.5 Assumptions and Dependencies
- **Assumptions:** Stable internet at 95% of sites, growing e-wallet adoption, API uptime ≥99.5%.
- **Dependencies:** API availability from GCash, Maya, telcos; cloud reliability; hardware supply chain.

---

## 3. Specific Requirements

### 3.1 Functional Requirements
*(Each requirement includes ID, title, priority, description, inputs, process, outputs, and acceptance criteria.)*

#### 3.1.1 WiFi Access Management
- **REQ-F-001:** WiFi Session Creation  
- **REQ-F-002:** Concurrent Session Management  
- **REQ-F-003:** Automatic Session Termination  
- **REQ-F-004:** Bandwidth Management  

#### 3.1.2 Payment Processing
- **REQ-F-005:** Multiple Payment Method Support  
- **REQ-F-006:** Coin Payment Processing  
- **REQ-F-007:** GCash Payment Processing  
- **REQ-F-008:** Maya Payment Processing  
- **REQ-F-009:** Payment Amount Validation  
- **REQ-F-010:** Digital Receipt Generation  

#### 3.1.3 Payment-First Whitelisting
- **REQ-F-011:** Pre-Payment Limited Access  
- **REQ-F-012:** Payment App Domain Whitelisting  
- **REQ-F-013:** Pre-Payment Access Time Limit  
- **REQ-F-014:** Full Access Activation  

#### 3.1.4 Additional Services
- **REQ-F-015:** Mobile Load Top-up Service  
- **REQ-F-016:** GCash Wallet Cash-in  
- **REQ-F-017:** Maya Wallet Cash-in  
- **REQ-F-018:** Utility Bills Payment  
- **REQ-F-019:** Gaming Credits Distribution  

#### 3.1.5 Customer Loyalty Program
- **REQ-F-020:** Customer Loyalty Card System  
- **REQ-F-021:** Loyalty Points Earning  
- **REQ-F-022:** Loyalty Points Redemption  

#### 3.1.6 Dynamic Advertising System
- **REQ-F-023:** Dynamic Advertisement Display  
- **REQ-F-024:** Advertisement Content Management  
- **REQ-F-025:** Advertisement Performance Analytics  

#### 3.1.7 System Management
- **REQ-F-026:** Real-time System Monitoring  
- **REQ-F-027:** Remote System Configuration  
- **REQ-F-028:** Business Performance Analytics  

### 3.2 Non-Functional Requirements

#### 3.2.1 Performance
- **REQ-NF-001:** Concurrent User Support  
- **REQ-NF-002:** Payment Transaction Response Time  
- **REQ-NF-003:** System Startup Performance  
- **REQ-NF-004:** Dashboard Performance  

#### 3.2.2 Security
- **REQ-NF-005:** Payment Transaction Security  
- **REQ-NF-006:** Secure API Access  
- **REQ-NF-007:** User Session Security  
- **REQ-NF-008:** Transaction Audit Trail  

#### 3.2.3 Reliability
- **REQ-NF-009:** Service Uptime Requirement  
- **REQ-NF-010:** System Recovery Capability  
- **REQ-NF-011:** Offline Operation Support  
- **REQ-NF-012:** Automated Data Backup  

#### 3.2.4 Scalability
- **REQ-NF-013:** Backend Scalability  

---

## 4. Verification and Acceptance Criteria
*(To be developed — includes testing methods, pass/fail criteria, compliance checks.)*

---

## 5. Supporting Information
- Diagrams
- Mockups
- API Documentation Links
- Hardware Specifications


[← Back to Documentation Home](../index.md) | [Go to Context →](../context/padayon_fi_context.md)
