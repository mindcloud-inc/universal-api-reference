# <img src="https://images.mindcloud.co/apps/icons/favicon_1775072928400.png" alt="Bolna logo" width="28" height="28"> Bolna: Universal API

Bolna is a Voice AI platform for creating, configuring, and managing voice AI agents and related telephony resources through a REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/bolna/latest
- **Category:** Support / Contact Center
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.bolna.ai/
- **Vendor API docs:** https://www.bolna.ai/docs/api-reference/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get User Details](actions/get-user-details.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bolna/latest/actions/get-user-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Agent

| Action | Method | Description |
| --- | --- | --- |
| [Create Agent](actions/create-agent.md) | POST | Creates a new voice AI agent in Bolna. |
| [Get Agent](actions/get-agent.md) | GET | Retrieves a specific Bolna voice AI agent. |
| [List Agents](actions/list-agents.md) | GET | Retrieves all voice AI agents in your Bolna account. |
| [Patch Update Agent](actions/patch-update-agent.md) | PUT | Updates selected fields on an existing Bolna voice AI agent. |
| [Update Agent](actions/update-agent.md) | PUT | Updates an existing voice AI agent in Bolna. |

### Agent Delete Result

| Action | Method | Description |
| --- | --- | --- |
| [Delete Agent](actions/delete-agent.md) | DELETE | Deletes an existing voice AI agent from Bolna. |

### Agent Stop Result

| Action | Method | Description |
| --- | --- | --- |
| [Stop Agent Calls](actions/stop-agent-calls.md) | PUT | Stops queued calls for a specific Bolna agent. |

### Batch

| Action | Method | Description |
| --- | --- | --- |
| [List Agent Batches](actions/list-agent-batches.md) | GET | Retrieves all batches for a specific Bolna agent. |

### Execution

| Action | Method | Description |
| --- | --- | --- |
| [List All Agent Executions](actions/list-all-agent-executions.md) | GET | Retrieves execution records for a specific Bolna agent. |

### Knowledgebase

| Action | Method | Description |
| --- | --- | --- |
| [Create Knowledgebase from URL](actions/create-knowledgebase-from-url.md) | POST | Creates a new knowledgebase in Bolna from a URL. |
| [Get Knowledgebase](actions/get-knowledgebase.md) | GET | Retrieves a specific knowledgebase from your Bolna account. |
| [List All Knowledgebases](actions/list-all-knowledgebases.md) | GET | Retrieves all knowledgebases in your Bolna account. |

### Knowledgebase Delete Result

| Action | Method | Description |
| --- | --- | --- |
| [Delete Knowledgebase](actions/delete-knowledgebase.md) | DELETE | Deletes an existing knowledgebase from your Bolna account. |

### Phone Number

| Action | Method | Description |
| --- | --- | --- |
| [List Phone Numbers](actions/list-phone-numbers.md) | GET | Retrieves phone numbers configured in your Bolna account. |
| [Search Phone Numbers](actions/search-phone-numbers.md) | GET | Finds available phone numbers by region, locality, or pattern. |

### Provider

| Action | Method | Description |
| --- | --- | --- |
| [List Providers](actions/list-providers.md) | GET | Retrieves providers configured in your Bolna account. |

### Sip Trunk

| Action | Method | Description |
| --- | --- | --- |
| [List SIP Trunks](actions/list-sip-trunks.md) | GET | Retrieves SIP trunks configured in your Bolna account. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User Details](actions/get-user-details.md) | GET | Retrieves your Bolna account details and usage limits. |

### Violation

| Action | Method | Description |
| --- | --- | --- |
| [List Violations](actions/list-violations.md) | GET | Retrieves violations for your Bolna account. |

### Voice

| Action | Method | Description |
| --- | --- | --- |
| [List All Voices](actions/list-all-voices.md) | GET | Retrieves all voices available in your Bolna account. |

