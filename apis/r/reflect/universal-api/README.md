# <img src="https://images.mindcloud.co/apps/icons/reflect_1773693926126.png" alt="Reflect logo" width="28" height="28"> Reflect: Universal API

Capture notes, connect ideas, and organize thoughts in Reflect

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/reflect/latest
- **Category:** Productivity / Knowledge Management
- **Actions:** 7
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://reflect.app
- **Vendor API docs:** https://reflect.academy/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reflect/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (7)

### Books

| Action | Method | Description |
| --- | --- | --- |
| [List Books](actions/list-books.md) | GET | Retrieves books from a graph in Reflect. |

### Graphs

| Action | Method | Description |
| --- | --- | --- |
| [List Graphs](actions/list-graphs.md) | GET | Retrieves graphs from Reflect. |

### Links

| Action | Method | Description |
| --- | --- | --- |
| [Create Link](actions/create-link.md) | POST | Creates a new link in a Reflect graph. |
| [List Links](actions/list-links.md) | GET | Retrieves links from a graph in Reflect. |

### Notes

| Action | Method | Description |
| --- | --- | --- |
| [Append to Daily Note](actions/append-to-daily-note.md) | PUT | Appends text to a daily note in Reflect. |
| [Create Note](actions/create-note.md) | POST | Creates a new note in Reflect. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from Reflect. |

