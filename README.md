# AI Operations Manager
A Multi-Agent Business Workflow Automation System

## Overview

AI Operations Manager is a multi-agent AI-powered pre-sales automation system designed to automate customer qualification, requirement gathering, lead analysis, proposal generation, and human handoff.

The system uses WhatsApp as the customer communication channel and leverages AI agents to reduce manual effort in sales and business operations workflows.

---

## Problem Statement

Software agencies and service businesses spend significant time:

* Responding to initial customer inquiries
* Understanding project requirements
* Qualifying leads
* Preparing summaries for sales teams
* Creating proposal drafts

This project automates these tasks using AI-powered workflow automation while keeping humans involved for final review and approval.

---

## Solution

The system acts as an AI Pre-Sales Assistant.

When a customer sends a message through WhatsApp:

1. AI responds to customer queries.
2. AI gathers project requirements naturally.
3. AI extracts structured lead information.
4. Lead information is stored in persistent memory.
5. AI determines when a lead is qualified.
6. Additional AI agents generate:

   * Lead Summary
   * Proposal Draft
7. Sales team receives an email with all generated outputs.
8. Customer is informed that a human representative will continue the discussion.

---

## Technologies Used

### Workflow Automation

* Make.com

### Communication

* WhatsApp Cloud API

### AI Model

* DeepSeek V4 Flash

### Storage

* Make Data Store

### Notifications

* Email Integration

---

## System Architecture

Customer

↓

WhatsApp Cloud API

↓

Make.com Workflow Engine

↓

Customer Memory (Data Store)

↓

AI Qualification Agent

↓

Lead Summary Agent

↓

Proposal Draft Agent

↓

Email Notification

↓

Human Sales Representative

---

## Workflow

### New Customer Flow

1. Customer sends first WhatsApp message.
2. Webhook receives message.
3. Customer record is created.
4. AI responds with welcome message.
5. Conversation begins.

### Existing Customer Flow

1. Existing customer message received.
2. Customer record retrieved.
3. AI analyzes conversation context.
4. AI answers customer questions.
5. AI extracts lead information.
6. AI updates lead record.

### Qualified Lead Flow

1. Lead reaches QUALIFIED state.
2. Lead Summary Agent executes.
3. Proposal Draft Agent executes.
4. Sales team receives notification email.
5. Customer receives handoff message.
6. Lead state changes to WAITING_FOR_HUMAN.

---

## AI Agents

### Agent 1 — Lead Qualification Agent

Responsibilities:

* Answer customer questions
* Gather project requirements
* Extract structured information
* Qualify leads

Tracked Fields:

* company_name
* service_required
* budget
* timeline
* requirements

### Agent 2 — Lead Summary Agent

Responsibilities:

* Analyze collected lead information
* Generate concise lead summaries

Output:

* lead_summary

### Agent 3 — Proposal Draft Agent

Responsibilities:

* Generate proposal drafts
* Suggest project scope
* Suggest next steps

Output:

* proposal_draft

---

## Cost Analysis

### DeepSeek V4 Flash

Estimated cost assuming 1,000 leads per month:

* ~ $2-$5/ month

Estimated AI Cost:

* Approximately ₹191.49 - ₹478.73/ month

### Make.com

Estimated workflow cost assuming 1,000 leads:

* ~ •	$53–$91/month

* Approximately ₹5,074.55-₹8,712.90/ month
---

## Key Features

* WhatsApp-based customer interaction
* Persistent customer memory
* AI lead qualification
* Structured information extraction
* Multi-agent workflow
* Automated proposal generation
* Human-in-the-loop review
* Email notifications

---

## Scalability Considerations

Future improvements include:

* PostgreSQL or Supabase integration
* CRM integration (HubSpot, Zoho, Salesforce)
* RAG-based company knowledge base
* Multi-model AI routing
* Analytics dashboard
* Advanced proposal generation
* Agent orchestration frameworks

---

## Risks and Limitations

* AI hallucinations when information is unavailable
* Dependence on third-party APIs
* Increased workflow costs at very large scale
* Human review still required for final proposal approval

---

## Repository Structure

```text
AI-Operations-Manager/
│
├── README.md
│
├── docs/
│   └── AI_Operations_Manager_Assignment.pdf
│
├── screenshots/
│   ├── architecture-diagram.png
│   ├── make-workflow.png
│   ├── whatsapp-conversation.png
│   ├── lead-summary.png
│   ├── proposal-draft.png
│   └── email-notification.png
│
├── diagrams/
│   └── architecture-diagram.png
│
└── make-scenario/
    └── scenario-export.json
```

---

## Conclusion

This project demonstrates how AI agents can automate a significant portion of the pre-sales workflow while maintaining a human review layer. The architecture is cost-effective, scalable, and suitable for deployment in software agencies, consulting firms, and service businesses.
