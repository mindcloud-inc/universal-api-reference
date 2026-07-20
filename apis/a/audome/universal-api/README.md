# <img src="https://images.mindcloud.co/apps/icons/screenshot-2026-04-03-at-14_1775235644824.png" alt="Audome logo" width="28" height="28"> Audome: Universal API

Audome is an audio collaboration and project management platform for producers, engineers, and clients, centralizing file delivery, feedback, and version tracking.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/audome/latest
- **Category:** Content & Files / Storage
- **Actions:** 9
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://audome.com
- **Vendor API docs:** https://app.audome.com/api-documentation

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Projects](actions/list-projects.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/audome/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (9)

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Create Client Project](actions/create-client-project.md) | POST |  |
| [Get Client Project](actions/get-client-project.md) | GET |  |
| [List Client Projects](actions/list-client-projects.md) | GET |  |
| [List Projects](actions/list-projects.md) | GET | Retrieves project records from Audome. |

### Tags

| Action | Method | Description |
| --- | --- | --- |
| [Create Tag List](actions/create-tag-list.md) | POST | Creates a new tag list in Audome. |
| [Delete Tag List](actions/delete-tag-list.md) | DELETE | Deletes an existing tag list from Audome. |
| [Get Tag List](actions/get-tag-list.md) | GET | Retrieves one tag list from Audome. |
| [List Tag Lists](actions/list-tag-lists.md) | GET | Retrieves tag list records from Audome. |
| [Update Tag List](actions/update-tag-list.md) | PUT | Updates an existing tag list in Audome. |

