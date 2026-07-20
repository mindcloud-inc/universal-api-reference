# <img src="https://images.mindcloud.co/apps/icons/bannerbite_1782739355112.png" alt="Bannerbite logo" width="28" height="28"> Bannerbite: Universal API

Bannerbite auto-generates bite-sized images and videos from projects, bites, and render jobs through its public REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/bannerbite/latest
- **Category:** Marketing
- **Actions:** 7
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://bannerbite.com
- **Vendor API docs:** https://developer.bannerbite.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Projects](actions/list-projects.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bannerbite/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (7)

### Bite

| Action | Method | Description |
| --- | --- | --- |
| [Get Bite](actions/get-bite.md) | GET | Retrieves a bite from Bannerbite by ID. |
| [List Bites](actions/list-bites.md) | GET | Retrieves bites from a Bannerbite project. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Get Project](actions/get-project.md) | GET | Retrieves a project from Bannerbite by ID. |
| [List Projects](actions/list-projects.md) | GET | Retrieves a list of projects from Bannerbite. |

### Render Job

| Action | Method | Description |
| --- | --- | --- |
| [Generate Image Or Video](actions/generate-image-or-video.md) | POST | Creates an image or video render job in Bannerbite. |
| [Render From Make](actions/render-from-make.md) | POST | Creates a Make render job in Bannerbite. |

### Scene Data

| Action | Method | Description |
| --- | --- | --- |
| [Get Scene Data](actions/get-scene-data.md) | GET | Retrieves scene data for a Bannerbite bite. |

