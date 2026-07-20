# <img src="https://images.mindcloud.co/apps/icons/tailwind-icon_1776455032810.png" alt="Tailwind logo" width="28" height="28"> Tailwind: Universal API

Tailwind lets you manage Pinterest publishing through Tailwind by listing connected accounts, browsing boards and smart schedule timeslots, and creating, scheduling, reviewing, or deleting posts.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/tailwind/latest
- **Category:** Marketing / Social Media
- **Actions:** 10
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.tailwindapp.com
- **Vendor API docs:** https://api-docs.tailwind.ai/getting-started/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Accounts](actions/list-accounts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tailwind/latest/actions/list-accounts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (10)

### Accounts

| Action | Method | Description |
| --- | --- | --- |
| [List Accounts](actions/list-accounts.md) | GET | Retrieves Pinterest accounts from Tailwind. |

### Board Lists

| Action | Method | Description |
| --- | --- | --- |
| [List Board Lists](actions/list-board-lists.md) | GET | Retrieves board lists from Tailwind. |

### Boards

| Action | Method | Description |
| --- | --- | --- |
| [List Boards](actions/list-boards.md) | GET | Retrieves boards from Tailwind. |

### Health Status

| Action | Method | Description |
| --- | --- | --- |
| [Health Check](actions/health-check.md) | GET | Retrieves Tailwind API health status. |

### Post

| Action | Method | Description |
| --- | --- | --- |
| [Create Post](actions/create-post.md) | POST | Creates a new post in Tailwind. |
| [Delete Post](actions/delete-post.md) | DELETE | Deletes an existing post from Tailwind. |
| [Get Post](actions/get-post.md) | GET | Retrieves a post from Tailwind. |
| [Schedule Post](actions/schedule-post.md) | PUT | Schedules an existing post in Tailwind. |

### Posts

| Action | Method | Description |
| --- | --- | --- |
| [List Posts](actions/list-posts.md) | GET | Retrieves posts from Tailwind. |

### Timeslots

| Action | Method | Description |
| --- | --- | --- |
| [List Timeslots](actions/list-timeslots.md) | GET | Retrieves publishing timeslots from Tailwind. |

