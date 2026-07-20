# <img src="https://images.mindcloud.co/apps/icons/app-wright_1771351967479.png" alt="AppWright logo" width="28" height="28"> AppWright: Universal API

AppWright through the MindCloud Universal API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/appWright/latest
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.appwright.com/
- **Vendor API docs:** https://docs.google.com/document/d/15cwpi-qdWiPcsSMziG8V41RzlJLw4yNqg0N0h_Em7xA/edit?tab=t.0

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Search SQL](actions/search-sql.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/appWright/latest/actions/search-sql?connectionId=$CONNECTION_ID&SQL=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Search

| Action | Method | Description |
| --- | --- | --- |
| [Search SQL](actions/search-sql.md) | GET | Retrieves AppWright data with a SQL select query. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Create Job](actions/create-job.md) | POST | Creates a new job in AppWright. |
| [Update Task Date](actions/update-task-date.md) | PUT | Updates a job task due date in AppWright. |

