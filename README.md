# ShopFlow Support – AI-Powered E-commerce Customer Support Agent

An AI-powered customer support agent built using **Salesforce Agentforce** as part of the Salesforce Unlocked Workshop at Amrita Vishwa Vidyapeetham, Nagercoil.

ShopFlow Support is designed to improve e-commerce customer service by handling common customer queries, assisting with orders and deliveries, managing support cases, and escalating unresolved issues.

## Project Overview

E-commerce businesses receive a large number of customer queries related to orders, delivery delays, returns, refunds, and account issues. Handling these requests manually can be time-consuming and lead to slower customer support.

ShopFlow Support aims to simplify this process through an AI-powered service agent that understands customer requests and routes them to the appropriate specialized subagent.

## Key Features

- **Customer Verification:** Uses email-based verification before accessing sensitive customer information.
- **Order Management:** Retrieves order information and supports order-related requests.
- **Delivery Assistance:** Handles delivery-related queries and delivery time-slot operations.
- **Return Management:** Explains return policies using available Knowledge sources and handles unavailable eligibility checks honestly.
- **Case Management:** Supports customer service case creation, lookup, and comments.
- **Account Management:** Supports contact information updates and secure password reset operations.
- **Knowledge-Based Support:** Uses Salesforce Knowledge actions to answer frequently asked questions.
- **Human Escalation:** Routes frustrated customers and unresolved issues toward human support.

## Technology Stack

- Salesforce Agentforce
- Salesforce Lightning Platform
- Salesforce Flow
- Salesforce Knowledge
- Salesforce Service Cloud capabilities
- Agentforce Actions and Subagents

## Agent Architecture

ShopFlow Support uses a multi-agent architecture with a central Agent Router that directs customer requests to specialized subagents.

### Subagents

| Subagent | Responsibility |
|---|---|
| Agent Router | Understands requests and manages routing |
| Service Customer Verification | Verifies customer identity |
| General FAQ | Answers general questions |
| Case Management | Creates and retrieves support cases |
| Account Management | Handles account-related requests |
| Delivery Issues | Handles delivery problems |
| Order Inquiries | Handles order-related questions |
| Return Management | Handles return and refund queries |
| Escalation | Handles unresolved and frustrated customer interactions |
| Off Topic / Ambiguous Question | Handles unrelated or unclear requests |

## Security and Reliability

The agent is configured with customer privacy and trustworthy responses as priorities.

- Customer verification is required before accessing sensitive customer information.
- The agent must not expose another customer's data.
- It must not invent order status, refund details, or return eligibility.
- Actions must be confirmed before reporting successful completion.
- Unavailable capabilities must be communicated honestly.

## Testing and Validation

The ShopFlow Support agent successfully compiled in Salesforce Agentforce Builder with:

- **Compilation Errors:** 0
- **Compilation Warnings:** 0

Initial Preview testing confirmed:

- Welcome message and customer support introduction.
- Knowledge unavailability handled without fabricating a return policy.
- Customer verification requested before order-related information.
- Identity verification requested before reporting a damaged product.

Further end-to-end testing of verification email delivery, order retrieval, and case creation remains pending.

## Current Limitations

- Automated return eligibility checking is unavailable because the required Flow does not exist in the Salesforce org.
- Useful FAQ responses require published Salesforce Knowledge articles.
- Verification email delivery requires further investigation.
- Live-agent escalation requires appropriate Omni-Channel configuration.

## Project Screenshots

Screenshots of the Agentforce Builder configuration, subagents, routing, successful compilation, and Preview testing are available in the [`screenshots`](screenshots/) directory.

## Future Improvements

- Implement automated return eligibility checking.
- Complete verification email delivery configuration.
- Add and publish Knowledge articles.
- Configure Omni-Channel for live-agent escalation.
- Perform comprehensive end-to-end testing.
- Improve customer interaction and error handling.

## Project Information

**Project:** ShopFlow Support  
**Platform:** Salesforce Agentforce  
**Workshop:** Salesforce Unlocked  
**Institution:** Amrita Vishwa Vidyapeetham, Nagercoil  
**Developer:** Akash K

---

*Built as part of the Salesforce Unlocked Workshop to explore AI-powered customer service automation using Salesforce Agentforce.*
