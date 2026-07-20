# <img src="https://images.mindcloud.co/apps/icons/rapid-reg_1775159169729.png" alt="RapidReg logo" width="28" height="28"> RapidReg: Universal API

RapidReg API wrapper for account, registration, inventory, and brand management endpoints.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/rapidReg/latest
- **Category:** Commerce
- **Actions:** 4
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.rapidreg.com/
- **Vendor API docs:** https://rapidreg.com/developers

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account](actions/get-account.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rapidReg/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (4)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | GET | Retrieves account details from RapidReg. |

### Brand

| Action | Method | Description |
| --- | --- | --- |
| [List Brands](actions/list-brands.md) | GET | Retrieves brands from RapidReg. |

### Item

| Action | Method | Description |
| --- | --- | --- |
| [List Items](actions/list-items.md) | GET | Retrieves items from RapidReg. |

### Registration

| Action | Method | Description |
| --- | --- | --- |
| [List Registrations](actions/list-registrations.md) | GET | Retrieves registrations from RapidReg. |

