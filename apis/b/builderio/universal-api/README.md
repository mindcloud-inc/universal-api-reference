# <img src="https://images.mindcloud.co/apps/icons/builderio_1776262560392.png" alt="Builder.io logo" width="28" height="28"> Builder.io: Universal API

Manage Builder content, models, assets, and spaces

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/builderio/latest
- **Category:** Website & App Building / CMS
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.builder.io/
- **Vendor API docs:** https://www.builder.io/c/docs/api-intro

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Models](actions/list-models.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/builderio/latest/actions/list-models?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Models

| Action | Method | Description |
| --- | --- | --- |
| [List Models](actions/list-models.md) | GET | Retrieves content models from Builder.io Admin API. |

