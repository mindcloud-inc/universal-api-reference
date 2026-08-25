# <img src="https://images.mindcloud.co/apps/icons/image-2843-vectorized_1777572012208.png" alt="MindCloud logo" width="28" height="28"> MindCloud: Universal API

MindCloud through the MindCloud Universal API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/mindCloud/latest
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Users](actions/list-users.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mindCloud/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Create Company](actions/create-company.md) | POST |  |
| [List Companies](actions/list-companies.md) | GET |  |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [List Users](actions/list-users.md) | GET |  |

