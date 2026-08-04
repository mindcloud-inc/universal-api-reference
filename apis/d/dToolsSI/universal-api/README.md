# <img src="https://images.mindcloud.co/apps/icons/clip-path-group-2_1781888917815.png" alt="D-Tools SI logo" width="28" height="28"> D-Tools SI: Universal API

D-Tools SI through the MindCloud Universal API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/dToolsSI/latest
- **Actions:** 7
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor API docs:** https://api.d-tools.com/si/doc

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Client Info](actions/list-client-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dToolsSI/latest/actions/list-client-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (7)

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Archive Projects](actions/archive-projects.md) | POST |  |
| [Get Partial Project by Id](actions/get-partial-project.md) | GET |  |
| [Get Project by Id](actions/get-project.md) | GET |  |
| [List Client Info](actions/list-client-info.md) | GET | Get clients published by a SI user. |
| [List Subscribed Projects](actions/list-subscribed-projects.md) | GET |  |
| [Publish Projects](actions/publish-projects.md) | POST |  |
| [Update Project](actions/update-project.md) | POST |  |

