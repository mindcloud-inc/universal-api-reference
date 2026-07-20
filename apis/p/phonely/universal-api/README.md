# <img src="https://images.mindcloud.co/apps/icons/phonely-icon-filled-256_1774620935009.png" alt="Phonely logo" width="28" height="28"> Phonely: Universal API

Manage AI voice agents, calls, phone numbers, and knowledge bases

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/phonely/latest
- **Category:** Support / Contact Center
- **Actions:** 19
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.phonely.ai
- **Vendor API docs:** https://docs.phonely.ai/api-reference/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Agent](actions/get-agent.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/phonely/latest/actions/get-agent?connectionId=$CONNECTION_ID&uid=string&agentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (19)

### Agent

| Action | Method | Description |
| --- | --- | --- |
| [Duplicate Agent](actions/duplicate-agent.md) | POST | Creates a duplicate agent in Phonely. |
| [Get Agent](actions/get-agent.md) | GET | Retrieves an agent from Phonely. |
| [List Agents](actions/list-agents.md) | GET | Retrieves agents from Phonely. |
| [Update Agent](actions/update-agent.md) | PUT | Updates an agent in Phonely. |

### Calls

| Action | Method | Description |
| --- | --- | --- |
| [Get Call](actions/get-call.md) | GET | Retrieves a call from Phonely. |
| [List Calls](actions/list-calls.md) | GET | Retrieves calls for a Phonely agent. |
| [Set Post-Call Outcome](actions/set-post-call-outcome.md) | PUT | Updates a post-call outcome in Phonely. |

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Add Agent Documents](actions/add-agent-documents.md) | POST | Adds documents to a Phonely agent. |
| [Delete Agent Documents](actions/delete-agent-documents.md) | DELETE | Deletes agent documents from Phonely. |
| [List Agent Documents](actions/list-agent-documents.md) | GET | Retrieves agent documents from Phonely. |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [List Organizations](actions/list-organizations.md) | GET | Retrieves organizations from Phonely. |

### Pages

| Action | Method | Description |
| --- | --- | --- |
| [Add Agent Websites](actions/add-agent-websites.md) | POST | Adds websites to a Phonely agent. |
| [Delete Agent Websites](actions/delete-agent-websites.md) | DELETE | Deletes agent websites from Phonely. |
| [List Agent Websites](actions/list-agent-websites.md) | GET | Retrieves agent websites from Phonely. |

### Phone Numbers

| Action | Method | Description |
| --- | --- | --- |
| [Add Block List Numbers](actions/add-block-list-numbers.md) | POST | Adds phone numbers to the Phonely block list. |
| [Delete Block List Numbers](actions/delete-block-list-numbers.md) | DELETE | Deletes phone numbers from the Phonely block list. |
| [List Block List](actions/list-block-list.md) | GET | Retrieves blocked phone numbers from Phonely. |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Get Usage](actions/get-usage.md) | GET | Retrieves usage from Phonely. |

### Voices

| Action | Method | Description |
| --- | --- | --- |
| [List Voices](actions/list-voices.md) | GET | Retrieves voices from Phonely. |

