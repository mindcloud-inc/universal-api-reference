# <img src="https://images.mindcloud.co/apps/icons/images-1_1775827543285.png" alt="Shotstack logo" width="28" height="28"> Shotstack: Universal API

Render videos, manage templates, and handle media assets with Shotstack

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/shotstack/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 18
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://shotstack.io
- **Vendor API docs:** https://shotstack.io/docs/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Templates](actions/list-templates.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shotstack/latest/actions/list-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (18)

### Asset

| Action | Method | Description |
| --- | --- | --- |
| [Delete Asset](actions/delete-asset.md) | DELETE |  |
| [Get Asset](actions/get-asset.md) | GET |  |
| [Get Asset by Render ID](actions/get-asset-by-render-id.md) | GET |  |
| [Transfer Asset](actions/transfer-asset.md) | POST |  |

### Media

| Action | Method | Description |
| --- | --- | --- |
| [Inspect Media](actions/inspect-media.md) | GET |  |

### Render Job

| Action | Method | Description |
| --- | --- | --- |
| [Get Render Status](actions/get-render-status.md) | GET |  |
| [Render Asset](actions/render-asset.md) | POST |  |

### Source

| Action | Method | Description |
| --- | --- | --- |
| [Delete Source](actions/delete-source.md) | DELETE |  |
| [Fetch Source](actions/fetch-source.md) | POST |  |
| [Get Source](actions/get-source.md) | GET |  |
| [List Sources](actions/list-sources.md) | GET |  |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [Create Template](actions/create-template.md) | POST |  |
| [Delete Template](actions/delete-template.md) | DELETE |  |
| [List Templates](actions/list-templates.md) | GET |  |
| [Render Template](actions/render-template.md) | POST |  |
| [Retrieve Template](actions/retrieve-template.md) | GET |  |
| [Update Template](actions/update-template.md) | PUT |  |

### Upload

| Action | Method | Description |
| --- | --- | --- |
| [Direct Upload](actions/direct-upload.md) | POST |  |

