# <img src="https://images.mindcloud.co/apps/icons/hyper-done_1775838005987.png" alt="HyperDone logo" width="28" height="28"> HyperDone: Universal API

Plan tasks on calendar boards, automate workflows, and collaborate with teams

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/hyperDone/latest
- **Category:** Productivity / Project Management
- **Actions:** 5
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://hyperdone.com/
- **Vendor API docs:** https://help.hyperdone.com/public-api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Board Info](actions/get-board-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hyperDone/latest/actions/get-board-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (5)

### Board

| Action | Method | Description |
| --- | --- | --- |
| [Get Board Info](actions/get-board-info.md) | GET |  |

### Board Member

| Action | Method | Description |
| --- | --- | --- |
| [List Board Members](actions/list-board-members.md) | GET |  |

### Column

| Action | Method | Description |
| --- | --- | --- |
| [List Columns](actions/list-columns.md) | GET |  |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [List Tags](actions/list-tags.md) | GET |  |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST |  |

