# Merge (merge)

Merge is the connective infrastructure for production AI. The Merge Unified API offers one API surface across HRIS, ATS, Accounting, CRM, Ticketing, File Storage, Knowledge Base, and Chat. Merge Agent Handler exposes pre-built enterprise connectors to AI agents via REST + MCP. Merge Gateway provides a unified LLM API across OpenAI, Anthropic, Google, Mistral, Cohere, and xAI with routing, caching, and observability.

**URL:** [Visit APIs.json URL](https://raw.githubusercontent.com/api-evangelist/merge/refs/heads/main/apis.yml)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=company-api-evangelist&utm_content=repo)

## Tags

 - Integrations, Platform, Unified API, Agent Handler, LLM Gateway

## Timestamps

- **Created:** 2025-06-05
- **Modified:** 2026-05-22

## Product Lines

Merge ships three product surfaces:

1. **Merge Unified API** — One API across HRIS, ATS, Accounting, CRM, Ticketing, File Storage, Knowledge Base, and Chat. Hosted on `api.merge.dev` (also `api-eu.merge.dev`, `api-ap.merge.dev`). Bearer + `X-Account-Token` auth.
2. **Merge Agent Handler** — Agentic tool orchestration with pre-built enterprise connectors. Management plane via REST at `ah-api.merge.dev`; agent-facing surface via MCP.
3. **Merge Gateway** — Unified LLM API on `api-gateway.merge.dev` routing to OpenAI, Anthropic, Google, Mistral, Cohere, and xAI. BYOK pricing is $0.05 per million tokens routed.

The provider publishes an RFC 9727 [`.well-known/api-catalog`](https://docs.merge.dev/.well-known/api-catalog) linking OpenAPI specs for all 10 surfaces above — captured locally in `openapi/`.

## APIs

### Merge HRIS API

Merge HRIS API provides a unified interface to integrate every HR, payroll, and SCIM directory system with one API. It normalizes data across 80+ HR platforms including Workday, BambooHR, Gusto, Rippling, ADP, and UKG Pro.

**Human URL:** https://www.merge.dev/categories/hr-payroll-api
**Base URL:** `https://api.merge.dev/api/hris/v1`

Properties: [Website](https://www.merge.dev/categories/hr-payroll-api) · [Documentation](https://docs.merge.dev/merge-unified/hris/overview) · [OpenAPI](openapi/merge-hris-api-openapi.yaml) · [JSONSchema](json-schema/hris-api-employee-schema.json) · [JSONStructure](json-structure/hris-api-employee-structure.json) · [JSON-LD](json-ld/merge-hris-api-context.jsonld) · [Example](examples/hris-api-employee-example.json)

Capabilities: hris-benefits · hris-companies · hris-employees · hris-employments · hris-groups · hris-locations · hris-payroll · hris-teams · hris-time-off

### Merge ATS API

Merge ATS API enables connection to every applicant tracking system with one API. It provides standardized data schemas for candidates, applications, interviews, and job postings across 50+ recruiting platforms including Greenhouse, Lever, Workday, iCIMS, and Jobvite.

**Human URL:** https://www.merge.dev/categories/ats-recruiting-api
**Base URL:** `https://api.merge.dev/api/ats/v1`

Properties: [Website](https://www.merge.dev/categories/ats-recruiting-api) · [Documentation](https://docs.merge.dev/merge-unified/ats/overview) · [OpenAPI](openapi/merge-ats-api-openapi.yaml) · [JSONSchema candidate](json-schema/ats-api-candidate-schema.json) · [JSONSchema application](json-schema/ats-api-application-schema.json) · [JSONStructure](json-structure/ats-api-candidate-structure.json) · [JSON-LD](json-ld/merge-ats-api-context.jsonld) · [Example candidate](examples/ats-api-candidate-example.json) · [Example application](examples/ats-api-application-example.json)

Capabilities: ats-activities · ats-applications · ats-candidates · ats-departments · ats-eeocs · ats-interviews · ats-jobs · ats-offers · ats-offices · ats-scorecards · ats-tags · ats-users

### Merge Accounting API

Merge Accounting API provides a unified API for accounting integrations across QuickBooks Online, Xero, NetSuite, Sage Intacct, and (April 2026 beta) Oracle Fusion Cloud ERP. It supports journal entries, payments, invoices, and other financial transaction data.

**Human URL:** https://www.merge.dev/categories/accounting-api
**Base URL:** `https://api.merge.dev/api/accounting/v1`

Properties: [Website](https://www.merge.dev/categories/accounting-api) · [Documentation](https://docs.merge.dev/merge-unified/accounting/overview) · [OpenAPI](openapi/merge-accounting-api-openapi.yaml) · [JSONSchema](json-schema/accounting-api-invoice-schema.json) · [JSONStructure](json-structure/accounting-api-invoice-structure.json) · [JSON-LD](json-ld/merge-accounting-api-context.jsonld) · [Example](examples/accounting-api-invoice-example.json)

Capabilities: accounts · company-info · contacts · credit-notes · expenses · financial-statements · invoices · items · journal-entries · payments · purchase-orders · tax-rates · tracking-categories · vendor-credits

### Merge Ticketing API

Merge Ticketing API provides unified access to 30+ ticketing and project management systems including Jira, Asana, Linear, Zendesk, Freshdesk, GitHub Issues, and ServiceNow.

**Human URL:** https://www.merge.dev/categories/ticketing-api
**Base URL:** `https://api.merge.dev/api/ticketing/v1`

Properties: [Website](https://www.merge.dev/categories/ticketing-api) · [Documentation](https://docs.merge.dev/merge-unified/ticketing/overview) · [OpenAPI](openapi/merge-ticketing-api-openapi.yaml) · [JSONSchema](json-schema/ticketing-api-ticket-schema.json) · [JSONStructure](json-structure/ticketing-api-ticket-structure.json) · [JSON-LD](json-ld/merge-ticketing-api-context.jsonld) · [Example](examples/ticketing-api-ticket-example.json)

Capabilities: ticketing-attachments · ticketing-comments · ticketing-contacts · ticketing-projects · ticketing-tags · ticketing-teams · ticketing-tickets · ticketing-users

### Merge CRM API

Merge CRM API provides unified access to 20+ CRM platforms including Salesforce, HubSpot, Pipedrive, and Zoho CRM, with custom object support.

**Human URL:** https://www.merge.dev/categories/crm-api
**Base URL:** `https://api.merge.dev/api/crm/v1`

Properties: [Website](https://www.merge.dev/categories/crm-api) · [Documentation](https://docs.merge.dev/merge-unified/crm/overview) · [OpenAPI](openapi/merge-crm-api-openapi.yaml) · [JSONSchema](json-schema/crm-api-opportunity-schema.json) · [JSONStructure](json-structure/crm-api-opportunity-structure.json) · [JSON-LD](json-ld/merge-crm-api-context.jsonld) · [Example](examples/crm-api-opportunity-example.json)

Capabilities: crm-accounts · crm-contacts · crm-engagements · crm-leads · crm-notes · crm-opportunities · crm-stages · crm-users

### Merge File Storage API

Merge File Storage API provides unified access to Box, Dropbox, Google Drive, OneDrive, and SharePoint. Includes a built-in File Picker for browsing connected storage accounts.

**Human URL:** https://www.merge.dev/categories/file-storage-api
**Base URL:** `https://api.merge.dev/api/filestorage/v1`

Properties: [Website](https://www.merge.dev/categories/file-storage-api) · [Documentation](https://docs.merge.dev/merge-unified/filestorage/overview) · [OpenAPI](openapi/merge-file-storage-api-openapi.yaml) · [JSONSchema](json-schema/file-storage-api-file-schema.json) · [JSONStructure](json-structure/file-storage-api-file-structure.json) · [JSON-LD](json-ld/merge-file-storage-api-context.jsonld) · [Example](examples/file-storage-api-file-example.json)

Capabilities: file-storage-drives · file-storage-files · file-storage-folders · file-storage-groups · file-storage-users

### Merge Knowledge Base API

Merge Knowledge Base API provides unified access to Confluence and Notion (Notion added February 2026). It normalizes Articles, Attachments, Containers, Groups, and Users with ACL management mapping users, groups, and company-level permissions across platforms — feeding enterprise AI context and search.

**Human URL:** https://www.merge.dev/categories/knowledge-base
**Base URL:** `https://api.merge.dev/api/knowledgebase/v1`

Properties: [Website](https://www.merge.dev/categories/knowledge-base) · [Documentation](https://docs.merge.dev/merge-unified/knowledge-base/overview) · [OpenAPI](openapi/merge-knowledge-base-api-openapi.yaml) · [JSONSchema](json-schema/knowledge-base-api-article-schema.json) · [JSONStructure](json-structure/knowledge-base-api-article-structure.json) · [JSON-LD](json-ld/merge-knowledge-base-api-context.jsonld) · [Example](examples/knowledge-base-api-article-example.json)

Capabilities: knowledge-base-articles · knowledge-base-attachments · knowledge-base-containers · knowledge-base-groups · knowledge-base-users

### Merge Chat API

Merge Chat Unified API (launched February 2026) provides real-time, normalized access to chat and messaging platforms starting with Microsoft Teams, with Slack on the roadmap. It normalizes five core object types — Messages, Conversations, Users, Groups, and Members.

**Human URL:** https://www.merge.dev/categories/chat
**Base URL:** `https://api.merge.dev/api/chat/v1`

Properties: [Website](https://www.merge.dev/categories/chat) · [Documentation](https://docs.merge.dev/merge-unified/chat/overview) · [OpenAPI](openapi/merge-chat-api-openapi.yaml) · [JSONSchema](json-schema/chat-api-message-schema.json) · [JSONStructure](json-structure/chat-api-message-structure.json) · [JSON-LD](json-ld/merge-chat-api-context.jsonld) · [Example](examples/chat-api-message-example.json)

Capabilities: chat-conversations · chat-messages · chat-users · chat-groups

### Merge Agent Handler

Merge Agent Handler enables AI agents to connect with thousands of pre-built tools for taking real-time actions. It manages authentication, rate limits, error handling, Tool Packs that group connectors per agent, Registered Users for end-user identity, and security controls (standard entity rules + custom regex rules) that scan tool inputs and responses for sensitive data. Exposes both a REST management API and an MCP server surface the agent talks to directly.

**Human URL:** https://www.merge.dev/merge-agent-handler
**Base URL:** `https://ah-api.merge.dev/api/v1`

Properties: [Website](https://www.merge.dev/merge-agent-handler) · [Documentation](https://docs.merge.dev/merge-agent-handler/agent-handler) · [OpenAPI](openapi/merge-agent-handler-api-openapi.yaml) · [JSONSchema](json-schema/agent-handler-tool-pack-schema.json) · [JSONStructure](json-structure/agent-handler-tool-pack-structure.json) · [JSON-LD](json-ld/merge-agent-handler-context.jsonld) · [Example](examples/agent-handler-tool-pack-example.json) · [Support](https://help.ah.merge.dev/)

Capabilities: agent-handler-connectors · agent-handler-tool-packs · agent-handler-registered-users · agent-handler-access-keys · agent-handler-security-rules

### Merge Gateway

Merge Gateway is a control plane for production AI providing unified access to OpenAI, Anthropic, Google (Gemini), Mistral, Cohere, and xAI (Grok) through a single API. It offers intelligent routing on cost/latency/quality, context compression, response caching, spend limits by team/project/customer, request-level logging, and automatic failover. BYOK billing is $0.05 per million tokens.

**Human URL:** https://www.merge.dev/gateway
**Base URL:** `https://api-gateway.merge.dev`

Properties: [Website](https://www.merge.dev/gateway) · [Documentation](https://docs.merge.dev/merge-gateway/api-overview) · [OpenAPI](openapi/merge-gateway-api-openapi.yaml) · [JSONSchema](json-schema/gateway-response-schema.json) · [JSONStructure](json-structure/gateway-response-structure.json) · [JSON-LD](json-ld/merge-gateway-context.jsonld) · [Example](examples/gateway-response-example.json)

Capabilities: gateway-models · gateway-responses · gateway-routing

## SDKs and tooling

Unified clients live under [github.com/merge-api](https://github.com/merge-api):

- Python: [merge-python-client](https://github.com/merge-api/merge-python-client)
- Node/TypeScript: [merge-node-client](https://github.com/merge-api/merge-node-client)
- Go: [merge-go-client](https://github.com/merge-api/merge-go-client)
- Java: [merge-java-client](https://github.com/merge-api/merge-java-client)
- Ruby: [merge-ruby-client](https://github.com/merge-api/merge-ruby-client)
- C#: [merge-csharp-client](https://github.com/merge-api/merge-csharp-client)
- Kotlin: [merge-sdk-kotlin](https://github.com/merge-api/merge-sdk-kotlin)

Agent / Gateway / MCP tooling:

- [merge-mcp](https://github.com/merge-api/merge-mcp) — Python MCP server for the Merge Unified API
- [merge-unified-skills](https://github.com/merge-api/merge-unified-skills) — Claude Code skills for the Unified API
- [merge-gateway-skills](https://github.com/merge-api/merge-gateway-skills) — Claude Code skills for Gateway
- [merge-gateway-ai-sdk-provider](https://github.com/merge-api/merge-gateway-ai-sdk-provider) — Vercel AI SDK provider
- [ah-plugins](https://github.com/merge-api/ah-plugins) — Agent Handler plugins for AI coding agents
- [react-merge-link](https://github.com/merge-api/react-merge-link), [vue-merge-link](https://github.com/merge-api/vue-merge-link), [react-agent-handler-link](https://github.com/merge-api/react-agent-handler-link), [react-agent-handler-chat](https://github.com/merge-api/react-agent-handler-chat), [agent-handler-chat-demo](https://github.com/merge-api/agent-handler-chat-demo)
- [n8n-nodes-merge](https://github.com/merge-api/n8n-nodes-merge) — n8n nodes for workflow automation

## Pricing & limits

Plans captured in [plans/merge-plans-pricing.yml](plans/merge-plans-pricing.yml):

- **Launch** — first 3 production Linked Accounts free; $650/mo for up to 10; $65 per additional. 100 req/min, 3-day log retention.
- **Professional** — contract pricing. 400 req/min, 30-day log retention, custom fields, field-level scopes.
- **Enterprise** — contract pricing. 600 req/min, 90+ day log retention, Audit Trail, dedicated CSM + Slack channel.
- **Agent Handler** — consumption-based after a free tier allocation.
- **Gateway (BYOK)** — $0.05 per million tokens routed.

Rate limits, FinOps mapping, and Spectral rules:

- [rate-limits/merge-rate-limits.yml](rate-limits/merge-rate-limits.yml)
- [finops/merge-finops.yml](finops/merge-finops.yml)
- [rules/merge-spectral-rules.yml](rules/merge-spectral-rules.yml)
- [vocabulary/merge-vocabulary.yaml](vocabulary/merge-vocabulary.yaml)

## Operations

- Status page: https://status.merge.dev/
- Trust center: https://trust.merge.dev/
- Compliance: SOC 2 Type 2, ISO 27001, GDPR, HIPAA-ready
- Changelog: https://www.merge.dev/changelog
