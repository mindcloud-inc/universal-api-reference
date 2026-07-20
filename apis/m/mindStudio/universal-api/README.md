# <img src="https://images.mindcloud.co/apps/icons/mind-studio_1774381623870.png" alt="MindStudio logo" width="28" height="28"> MindStudio: Universal API

Run, embed, and integrate MindStudio AI agents

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/mindStudio/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://app.mindstudio.ai
- **Vendor API docs:** https://university.mindstudio.ai/docs/developers/api-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Load App](actions/load-app.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mindStudio/latest/actions/load-app?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### App

| Action | Method | Description |
| --- | --- | --- |
| [Load App](actions/load-app.md) | GET | Retrieves app details from MindStudio. |

### App Run

| Action | Method | Description |
| --- | --- | --- |
| [Run App](actions/run-app.md) | POST | Runs an app in MindStudio. |

### Signed Access Url

| Action | Method | Description |
| --- | --- | --- |
| [Generate Signed Access URL](actions/generate-signed-access-url.md) | POST | Creates a signed access URL for a MindStudio agent. |

