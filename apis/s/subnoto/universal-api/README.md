# <img src="https://images.mindcloud.co/apps/icons/images_1775844750857.jpeg" alt="Subnoto logo" width="28" height="28"> Subnoto: Universal API

Subnoto: Send, sign, and manage confidential agreements

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/subnoto/latest
- **Category:** Productivity / Legal & Contracts
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://subnoto.com
- **Vendor API docs:** https://subnoto.com/documentation

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Who Am I](actions/who-am-i.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/subnoto/latest/actions/who-am-i?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Team

| Action | Method | Description |
| --- | --- | --- |
| [Who Am I](actions/who-am-i.md) | GET |  |

### Workspace

| Action | Method | Description |
| --- | --- | --- |
| [List Workspaces](actions/list-workspaces.md) | GET |  |

