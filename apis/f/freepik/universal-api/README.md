# <img src="https://images.mindcloud.co/apps/icons/freepik_1776266882952.png" alt="Freepik logo" width="28" height="28"> Freepik: Universal API

Search, retrieve, download, and generate creative assets

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/freepik/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.freepik.com/
- **Vendor API docs:** https://docs.freepik.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Search Resources](actions/search-resources.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freepik/latest/actions/search-resources?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Icon

| Action | Method | Description |
| --- | --- | --- |
| [Get Icon](actions/get-icon.md) | GET | Retrieves detailed icon information from Freepik. |
| [Search Icons](actions/search-icons.md) | GET | Finds Freepik icons by search term and filters. |

### Icon Download

| Action | Method | Description |
| --- | --- | --- |
| [Download Icon](actions/download-icon.md) | GET | Retrieves a Freepik icon download URL. |

### Lora

| Action | Method | Description |
| --- | --- | --- |
| [List LoRAs](actions/list-loras.md) | GET |  |

### Music Download

| Action | Method | Description |
| --- | --- | --- |
| [Download Music](actions/download-music.md) | GET | Retrieves a Freepik music download URL. |

### Music Track

| Action | Method | Description |
| --- | --- | --- |
| [Get Music](actions/get-music.md) | GET | Retrieves detailed music information from Freepik. |
| [Search Music](actions/search-music.md) | GET | Finds Freepik music by search term and filters. |

### Prompt Improvement Task

| Action | Method | Description |
| --- | --- | --- |
| [Improve Prompt](actions/improve-prompt.md) | POST |  |

### Resource

| Action | Method | Description |
| --- | --- | --- |
| [Get Resource](actions/get-resource.md) | GET | Retrieves detailed resource information from Freepik. |
| [Search Resources](actions/search-resources.md) | GET | Finds Freepik resources by search term and filters. |

### Resource Download

| Action | Method | Description |
| --- | --- | --- |
| [Download Resource](actions/download-resource.md) | GET | Retrieves a Freepik resource download URL. |

### Resource Download Format

| Action | Method | Description |
| --- | --- | --- |
| [Get Resource Download Format](actions/get-resource-download-format.md) | GET | Retrieves a Freepik resource download in a specified format. |

### Sound Effect

| Action | Method | Description |
| --- | --- | --- |
| [Get Sound Effect](actions/get-sound-effect.md) | GET |  |
| [Search Sound Effects](actions/search-sound-effects.md) | GET |  |

### Sound Effect Download

| Action | Method | Description |
| --- | --- | --- |
| [Download Sound Effect](actions/download-sound-effect.md) | GET |  |

### Video

| Action | Method | Description |
| --- | --- | --- |
| [Get Video](actions/get-video.md) | GET | Retrieves detailed video information from Freepik. |
| [Search Videos](actions/search-videos.md) | GET | Finds Freepik videos by search term and filters. |

### Workflow App

| Action | Method | Description |
| --- | --- | --- |
| [Get Workflow App](actions/get-workflow-app.md) | GET |  |
| [List My Workflow Apps](actions/list-my-workflow-apps.md) | GET |  |
| [List Workflow Apps](actions/list-workflow-apps.md) | GET |  |

