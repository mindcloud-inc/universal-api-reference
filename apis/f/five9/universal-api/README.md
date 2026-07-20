# <img src="https://images.mindcloud.co/apps/icons/five9_1754418597631.png" alt="Five9 logo" width="28" height="28"> Five9: Universal API

Five9 through the MindCloud Universal API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/five9/latest
- **Category:** Support / Contact Center
- **Actions:** 5
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor API docs:** https://documentation.five9.com/bundle/admin-console/page/admin-console/landing-admin-console.htm

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Campaign Settings](actions/campaign-settings.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/five9/latest/actions/campaign-settings?connectionId=$CONNECTION_ID&domainID=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (5)

### Campaigns

| Action | Method | Description |
| --- | --- | --- |
| [Campaign Settings](actions/campaign-settings.md) | GET |  |

### Employees

| Action | Method | Description |
| --- | --- | --- |
| [Create User](actions/create-users.md) | POST |  |
| [My User Permission's](actions/my-user-permissions.md) | GET | Retrieves your user permissions from Five9. |
| [Update User](actions/update-user-info.md) | PUT | Updates an existing user in Five9. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [List Users](actions/list-users.md) | GET | Retrieves users from Five9. |

