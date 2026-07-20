# <img src="https://images.mindcloud.co/apps/icons/images-22_1776368678305.png" alt="Persona logo" width="28" height="28"> Persona: Universal API

Manage identity inquiries, accounts, cases, reports, and transactions

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/persona/latest
- **Category:** IT Operations / Security & Identity
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://app.withpersona.com
- **Vendor API docs:** https://docs.withpersona.com/api-keys

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Inquiries](actions/list-inquiries.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/persona/latest/actions/list-inquiries?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Add Account Tag](actions/add-account-tag.md) | PUT |  |
| [Create Account](actions/create-account.md) | POST |  |
| [List Accounts](actions/list-accounts.md) | GET |  |
| [Redact Account](actions/redact-account.md) | DELETE |  |
| [Remove Account Tag](actions/remove-account-tag.md) | PUT |  |
| [Retrieve Account](actions/retrieve-account.md) | GET |  |
| [Search Accounts](actions/search-accounts.md) | GET |  |
| [Update Account](actions/update-account.md) | PUT |  |

### Api Key

| Action | Method | Description |
| --- | --- | --- |
| [List API keys](actions/list-api-keys.md) | GET |  |

### Api Log

| Action | Method | Description |
| --- | --- | --- |
| [List API Logs](actions/list-api-logs.md) | GET |  |
| [Retrieve API Log](actions/retrieve-api-log.md) | GET |  |

### Case

| Action | Method | Description |
| --- | --- | --- |
| [List Cases](actions/list-cases.md) | GET |  |
| [Search Cases](actions/search-cases.md) | GET |  |

### Connect

| Action | Method | Description |
| --- | --- | --- |
| [List Connections](actions/list-connections.md) | GET |  |
| [List Share Tokens](actions/list-share-tokens.md) | GET |  |

### Device

| Action | Method | Description |
| --- | --- | --- |
| [List Devices](actions/list-devices.md) | GET |  |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [List Events](actions/list-events.md) | GET |  |
| [Retrieve Event](actions/retrieve-event.md) | GET |  |

### Importer

| Action | Method | Description |
| --- | --- | --- |
| [List Importers](actions/list-importers.md) | GET |  |

### Inquiry

| Action | Method | Description |
| --- | --- | --- |
| [List Inquiries](actions/list-inquiries.md) | GET |  |

### Inquiry Session

| Action | Method | Description |
| --- | --- | --- |
| [List Inquiry Sessions](actions/list-inquiry-sessions.md) | GET |  |

### Inquiry Template

| Action | Method | Description |
| --- | --- | --- |
| [List Inquiry Templates](actions/list-inquiry-templates.md) | GET |  |
| [Retrieve Inquiry Template](actions/retrieve-inquiry-template.md) | GET |  |

### List

| Action | Method | Description |
| --- | --- | --- |
| [List Lists](actions/list-lists.md) | GET |  |

### Rate Limit

| Action | Method | Description |
| --- | --- | --- |
| [List Rate Limits](actions/list-rate-limits.md) | GET |  |

### Report

| Action | Method | Description |
| --- | --- | --- |
| [List Reports](actions/list-reports.md) | GET |  |

### Transaction

| Action | Method | Description |
| --- | --- | --- |
| [List Transactions](actions/list-transactions.md) | GET |  |

### User Audit Log

| Action | Method | Description |
| --- | --- | --- |
| [List User Audit Logs](actions/list-user-audit-logs.md) | GET |  |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [List Webhooks](actions/list-webhooks.md) | GET |  |

### Workflow

| Action | Method | Description |
| --- | --- | --- |
| [List Workflow Runs](actions/list-workflow-runs.md) | GET |  |

