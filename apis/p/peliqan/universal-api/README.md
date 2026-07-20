# <img src="https://images.mindcloud.co/apps/icons/favicon-help-peliqan-io-48x48_1775761351112.png" alt="Peliqan logo" width="28" height="28"> Peliqan: Universal API

Manage Peliqan data warehouses, apps, groups, users, and queries

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/peliqan/latest
- **Category:** Business Intelligence / Data Warehouse
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://peliqan.io
- **Vendor API docs:** https://help.peliqan.io/peliqan-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/peliqan/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Application

| Action | Method | Description |
| --- | --- | --- |
| [List Applications](actions/list-applications.md) | GET | Retrieves applications from Peliqan. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from Peliqan. |

