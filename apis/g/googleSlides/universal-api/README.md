# <img src="https://images.mindcloud.co/apps/icons/google-slides-logo_1779812244921.png" alt="Google Slides logo" width="28" height="28"> Google Slides: Universal API

Create presentations, collaborate on slides, present live, and share recordings.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/googleSlides/latest
- **Category:** Content & Files / Storage
- **Actions:** 6
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://workspace.google.com/products/slides/
- **Vendor API docs:** https://developers.google.com/workspace/slides/api/reference/rest

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Presentation](actions/get-presentation.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleSlides/latest/actions/get-presentation?connectionId=$CONNECTION_ID&presentationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (6)

### Page

| Action | Method | Description |
| --- | --- | --- |
| [Get Page](actions/get-page.md) | GET | Retrieves a presentation page from Google Slides. |

### Presentation

| Action | Method | Description |
| --- | --- | --- |
| [Create Presentation](actions/create-presentation.md) | POST | Creates a new presentation in Google Slides. |
| [Delete Presentation](actions/delete-presentation.md) | DELETE | Deletes an existing presentation file from Google Slides. |
| [Get Presentation](actions/get-presentation.md) | GET | Retrieves a presentation from Google Slides. |
| [Update Presentation](actions/update-presentation.md) | PUT | Updates an existing presentation file in Google Slides. |

### Thumbnail

| Action | Method | Description |
| --- | --- | --- |
| [Get Page Thumbnail](actions/get-page-thumbnail.md) | GET | Retrieves a page thumbnail URL from Google Slides. |

