# <img src="https://images.mindcloud.co/apps/icons/clipcat-icon_1775766809670.png" alt="Clipcat logo" width="28" height="28"> Clipcat: Universal API

Clipcat generates video renders from reusable templates through its public REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/clipcat/latest
- **Category:** Marketing
- **Actions:** 7
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.clipcat.com
- **Vendor API docs:** https://developers.clipcat.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Authorization Status](actions/get-authorization-status.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clipcat/latest/actions/get-authorization-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (7)

### Render

| Action | Method | Description |
| --- | --- | --- |
| [Create Render](actions/create-render.md) | POST | Creates a new video render request in Clipcat. |
| [Get Render](actions/get-render.md) | GET | Retrieves a video render from Clipcat. |
| [List Renders](actions/list-renders.md) | GET | Retrieves video renders for the current Clipcat workspace. |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [Get Template](actions/get-template.md) | GET | Retrieves a video template from Clipcat. |
| [List Templates](actions/list-templates.md) | GET | Retrieves available video templates from Clipcat. |

### Workspace

| Action | Method | Description |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | GET | Retrieves account quota and usage details from Clipcat. |
| [Get Authorization Status](actions/get-authorization-status.md) | GET | Retrieves authorization status for the current Clipcat workspace. |

