# <img src="https://images.mindcloud.co/apps/icons/sipuni-icon_1776693067319.png" alt="Sipuni logo" width="28" height="28"> Sipuni: Universal API

Sipuni exposes telephony statistics exports and recording retrieval for Sipuni cloud PBX accounts.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/sipuni/latest
- **Category:** Support / Contact Center
- **Actions:** 6
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://sipuni.com
- **Vendor API docs:** https://doc.sipuni.com/articles/636--api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Operators](actions/list-operators.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sipuni/latest/actions/list-operators?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (6)

### Attachments

| Action | Method | Description |
| --- | --- | --- |
| [Get CRM Recording](actions/get-crm-recording.md) | GET |  |
| [Get Recording](actions/get-recording.md) | GET | Retrieves a call recording audio file from Sipuni. |

### Calls

| Action | Method | Description |
| --- | --- | --- |
| [Call Number](actions/call-number.md) | POST |  |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Export All Statistics](actions/export-all-statistics.md) | GET | Exports all call recording entries from Sipuni. |
| [Export Statistics](actions/export-statistics.md) | GET | Exports filtered call statistics from Sipuni. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [List Operators](actions/list-operators.md) | GET | Retrieves operators and presence statuses from Sipuni. |

