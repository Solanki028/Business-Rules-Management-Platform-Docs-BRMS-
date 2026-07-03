# Dynamic Pricing & Revenue Management Platform — Project Summary

This repository contains the core documentation and technical specifications for the **Dynamic Pricing & Revenue Management Platform**. 

For detailed information, please read the provided documents:
*   📄 **[DPP_Business_Discovery.pdf](DPP_Business_Discovery.pdf)** — Business Discovery & Market Research Report.
*   📄 **[DPP_FRD_SAD.pdf](DPP_FRD_SAD.pdf)** — Functional Requirements Document & System Architecture Design.
*   📝 **[Technical_Implementation_Specification.md](Technical_Implementation_Specification.md)** — Low-Level Design (LLD), Database Schemas, Rule/Pricing Engine Flows, and API Catalog.

---

## 1. What is this project?
This is an internal Dynamic Pricing & Revenue Management Platform for a cruise/travel company. It is not a booking website. Instead, it is a centralized platform where business teams can create, manage, simulate, approve, and publish pricing rules that are consumed by booking systems (Website, Mobile App, OTA, Partner APIs).

## 2. Why are we building this?
Travel inventory (cruise cabins, hotel rooms, flight seats) is perishable. If a cabin is not sold before departure, its value becomes zero. Static pricing cannot maximize revenue because demand changes continuously. 

Current problems include:
*   Manual pricing
*   Spreadsheet management
*   Revenue leakage
*   Multi-channel pricing complexity
*   Slow price updates
*   Human errors
*   Limited flexibility in existing RMS tools

The goal is to automate pricing decisions while allowing business users to configure rules without engineering involvement.

## 3. Existing Market Research
We researched existing Revenue Management Systems such as:
*   IDeaS
*   Duetto
*   Lighthouse
*   Atomize

These platforms already provide dynamic pricing, revenue optimization, demand forecasting, and reporting. However, they cannot fully support company-specific pricing logic, approval workflows, partner contracts, and custom business rules. That's why many enterprises build their own custom pricing platform.

## 4. Product Vision
The platform becomes the single source of truth for pricing. Business users should be able to do the following without writing code:
*   Create pricing rules
*   Configure promotions
*   Simulate prices
*   Approve rules
*   Publish rules
*   Track pricing history
*   Generate reports

## 5. Core Idea
The biggest realization during research was: **This is not just a Dynamic Pricing Tool; it is actually a Business Rules Management Platform (BRMS).** Pricing is only one category of business rules. The Rule Engine is the heart of the platform.

## 6. Business Requirements
The platform supports:
*   Seasonal & Holiday pricing
*   Occupancy & Booking window pricing
*   Customer segment & Platform-specific pricing
*   Promotions & Coupon campaigns
*   Manual overrides & Rule priorities
*   Rule scheduling & Price simulation
*   Audit logs & Analytics reports

## 7. Technical Architecture
Recommended architecture:
*   **Frontend:** React Dashboard
*   **Backend:** NestJS Backend (Modular Monolith, Domain-Driven Design)
*   **Database:** PostgreSQL
*   **Caching & Queues:** Redis & BullMQ
*   **Core Logic:** Rule Engine, Pricing Engine, and Simulation Engine
*   *Designed to scale from MVP to enterprise.*

## 8. Engineering Blueprint
The engineering blueprint defines:
*   Rule lifecycle & versioning
*   Rule builder & execution flow
*   Rule conflict resolution
*   Price simulation & cache strategy
*   Publish workflow
*   Growth architecture & engineering roadmap

## 9. Technical Implementation
The implementation document contains:
*   Database schema & ER diagrams
*   API design & folder structure
*   Authentication flow (JWT + RBAC)
*   Rule Engine, Pricing Engine, and Simulation Engine architecture
*   Redis strategy & Queue architecture
*   Security, Testing, and Sprint roadmap
*   *Acts as the backend implementation specification.*

## 10. Overall Deliverables
We have created:
1.  **Document 1: Business Discovery & Market Research** — *Answers: Why are we building this?*
2.  **Document 2: Functional Requirements** — *Answers: What should the product do?*
3.  **Document 3: System Architecture & Engineering Blueprint** — *Answers: How is the platform structured?*
4.  **Document 4: Technical Implementation Specification** — *Answers: How will engineers actually build it?*