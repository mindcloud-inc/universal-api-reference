# <img src="https://images.mindcloud.co/apps/icons/1200x630wa_1776776237518.jpeg" alt="Agicap logo" width="28" height="28"> Agicap: Universal API

Agicap is a cash flow, treasury, payments, accounts payable, and accounts receivable platform. Its public API supports Treasury Bank Journal exports and organization entity lookup.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/agicap/latest
- **Actions:** 4
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://agicap.com
- **Vendor API docs:** https://api.agicap.com/treasury-bank-journal/detailed_documentation.pdf

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Bank Journal Export Details](actions/get-bank-journal-export-details.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/agicap/latest/actions/get-bank-journal-export-details?connectionId=$CONNECTION_ID&entityId=140010&exportId=47a62f3d-6885-4f33-a7d2-40a4470b3a5f" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (4)

### Bank Journal Export

| Action | Method | Description |
| --- | --- | --- |
| [Create Bank Journal Export](actions/create-bank-journal-export.md) | POST | Creates a bank journal export in Agicap for ready-to-export entries. |
| [Get Bank Journal Export Details](actions/get-bank-journal-export-details.md) | GET | Retrieves details for a bank journal export from Agicap. |
| [List Bank Journal Exports](actions/list-bank-journal-exports.md) | GET | Retrieves previous bank journal exports from Agicap. |

### Organization Entity

| Action | Method | Description |
| --- | --- | --- |
| [List Organization Entities](actions/list-organization-entities.md) | GET | Retrieves organization entities for an Agicap organization. |

