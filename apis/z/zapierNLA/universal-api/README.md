# <img src="https://images.mindcloud.co/apps/icons/zapier-nla-icon_1776707348057.png" alt="Zapier NLA logo" width="28" height="28"> Zapier NLA: Universal API

Zapier NLA exposes Zapier AI Actions so users can search available automations, configure exposed actions, inspect exposed actions, and retrieve execution details through Zapier's natural-language action API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/zapierNLA/latest
- **Actions:** 8
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://nla.zapier.com/
- **Vendor API docs:** https://nla.zapier.com/api/v1/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Check Connection](actions/check-connection.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zapierNLA/latest/actions/check-connection?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (8)

### Action

| Action | Method | Description |
| --- | --- | --- |
| [List Directory Actions](actions/list-directory-actions.md) | GET |  |

### Configuration Link

| Action | Method | Description |
| --- | --- | --- |
| [Get Configuration Link](actions/get-configuration-link.md) | GET |  |

### Connection

| Action | Method | Description |
| --- | --- | --- |
| [Check Connection](actions/check-connection.md) | GET |  |

### Execution

| Action | Method | Description |
| --- | --- | --- |
| [Execute Dynamic Exposed Action](actions/execute-dynamic-exposed-action.md) | POST |  |
| [Execute Exposed Action](actions/execute-exposed-action.md) | POST |  |

### Execution Log

| Action | Method | Description |
| --- | --- | --- |
| [Get Execution Log](actions/get-execution-log.md) | GET |  |

### Exposed Action

| Action | Method | Description |
| --- | --- | --- |
| [List Exposed Actions](actions/list-exposed-actions.md) | GET |  |

### Guided Recipe

| Action | Method | Description |
| --- | --- | --- |
| [List Guided Recipes](actions/list-guided-recipes.md) | GET |  |

