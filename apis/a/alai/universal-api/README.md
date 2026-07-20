# <img src="https://images.mindcloud.co/apps/icons/alai_1775511661890.png" alt="Alai logo" width="28" height="28"> Alai: Universal API

Create, export, and manage presentations with Alai

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/alai/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 11
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://getalai.com
- **Vendor API docs:** https://docs.getalai.com/api/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Themes](actions/list-themes.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/alai/latest/actions/list-themes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (11)

### Export

| Action | Method | Description |
| --- | --- | --- |
| [Export Presentation](actions/export-presentation.md) | POST | Creates an async presentation export in Alai. |

### Generation

| Action | Method | Description |
| --- | --- | --- |
| [Get Generation Status](actions/get-generation-status.md) | GET | Retrieves async operation status from Alai. |

### Image

| Action | Method | Description |
| --- | --- | --- |
| [Upload Images](actions/upload-images.md) | POST | Uploads images to Alai and returns image IDs. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Verify API Key](actions/verify-api-key.md) | GET | Verifies API key access to Alai. |

### Presentation

| Action | Method | Description |
| --- | --- | --- |
| [Delete Presentation](actions/delete-presentation.md) | DELETE | Permanently deletes a presentation from Alai. |
| [Generate Presentation](actions/generate-presentation.md) | POST | Creates an async presentation generation in Alai from text input. |
| [List Presentations](actions/list-presentations.md) | GET | Retrieves presentations owned by the authenticated Alai user. |

### Slide

| Action | Method | Description |
| --- | --- | --- |
| [Create Slide](actions/create-slide.md) | POST | Creates an async slide generation in an Alai presentation. |
| [Delete Slide](actions/delete-slide.md) | DELETE | Permanently deletes a slide from an Alai presentation. |

### Theme

| Action | Method | Description |
| --- | --- | --- |
| [List Themes](actions/list-themes.md) | GET | Retrieves theme IDs and names from Alai. |

### Transcript

| Action | Method | Description |
| --- | --- | --- |
| [Extract Transcripts](actions/extract-transcripts.md) | POST | Creates an async transcript extraction for an Alai presentation. |

