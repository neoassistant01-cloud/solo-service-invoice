# Solo Service Invoice - Product Requirements

## Project Overview
- **Name:** Solo Service Invoice
- **Type:** Micro-SaaS (Self-hosted web app)
- **Core Functionality:** Dead-simple invoice creation for solo tradesmen (plumbers, electricians, HVAC) working in the field
- **Target Users:** Solo trades professionals who need to send professional invoices from their truck/phone

## Target Market
- **Vertical:** Trade services (plumbing, electrical, HVAC)
- **User Profile:** Solo operator, works from truck/field, needs mobile-first solution
- **Price Sensitivity:** $15-20/mo acceptable

## Problem Statement
Existing solutions (Jobber, ServiceTitan) are overkill for solo operators. Complex, expensive, feature-bloated. Tradesmen just need to:
1. Create invoice fast from phone
2. Send PDF to customer
3. Reuse saved customers
4. See simple earnings dashboard

## Requirements (REQ-###)

### REQ-001: Invoice Creation
- User can create new invoice with:
  - Customer name (required)
  - Customer address (required)
  - Service description (required)
  - Line items (service, quantity, rate) - dynamic add/remove
  - Auto-calculated total
- Invoice date auto-generated
- Invoice number auto-generated (INV-001, INV-002...)

### REQ-002: PDF Generation
- Generate professional PDF from invoice data
- Download to device
- Include: business name, customer info, line items, total, payment terms

### REQ-003: Customer Management
- Save customer list (localStorage)
- Select from saved customers on new invoice
- Edit/delete saved customers

### REQ-004: Dashboard
- Show total invoices created
- Show total revenue (sum of all invoices)
- Show recent invoices list
- Simple, at-a-glance metrics

### REQ-005: Business Info
- User can set business name (displayed on invoices)
- User can set contact info

### REQ-006: Mobile-First UI
- Clean, large-touch-targets interface
- Works on phone browser
- Responsive design

## Out of Scope (for MVP)
- Payment processing
- Email sending (just PDF download)
- Multi-user / team features
- Job scheduling
- Estimates/quotes

## Success Metrics
- Invoice creation time < 2 minutes
- PDF generates in < 3 seconds
- Mobile usable on 375px width
