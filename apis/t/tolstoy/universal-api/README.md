# <img src="https://images.mindcloud.co/apps/icons/tolstoy_1774976712420.png" alt="Tolstoy logo" width="28" height="28"> Tolstoy: Universal API

AI commerce platform for interactive video, shoppable content, and onsite shopping experiences.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/tolstoy/latest
- **Category:** Commerce
- **Actions:** 7
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.gotolstoy.com/
- **Vendor API docs:** https://developers.gotolstoy.com/welcome

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Videos](actions/list-videos.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tolstoy/latest/actions/list-videos?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (7)

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a new project in Tolstoy. |
| [Get Project](actions/get-project.md) | GET | Retrieves a specific project from Tolstoy. |

### Video

| Action | Method | Description |
| --- | --- | --- |
| [Create Video by URL](actions/create-video-by-url.md) | POST | Creates a new video in Tolstoy from a URL. |
| [List Videos](actions/list-videos.md) | GET | Retrieves all video records from Tolstoy. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Add Webhook](actions/add-webhook.md) | POST | Creates a new webhook in Tolstoy. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes an existing webhook from Tolstoy. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves all webhook records from Tolstoy. |

