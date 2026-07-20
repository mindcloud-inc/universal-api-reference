# <img src="https://images.mindcloud.co/apps/icons/jostle_1774893703504.png" alt="Jostle logo" width="28" height="28"> Jostle: Universal API

Connect employees, share updates, and find workplace information

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/jostle/latest
- **Actions:** 10
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://jostle.me
- **Vendor API docs:** https://api.jostle.me/docs/getting-started

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Enterprise Users](actions/list-enterprise-users.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jostle/latest/actions/list-enterprise-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (10)

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST |  |
| [Create Tasks for Many Assignees](actions/create-tasks-for-many-assignees.md) | POST |  |
| [Get Task](actions/get-task.md) | GET |  |
| [Update Task](actions/update-task.md) | PUT |  |

### Task Comment

| Action | Method | Description |
| --- | --- | --- |
| [Comment on Task](actions/comment-on-task.md) | POST |  |
| [List Task Comments](actions/list-task-comments.md) | GET |  |

### Task Comment Attachment

| Action | Method | Description |
| --- | --- | --- |
| [Attach File to Task Comment](actions/attach-file-to-task-comment.md) | POST |  |

### Task Preset

| Action | Method | Description |
| --- | --- | --- |
| [List Presets](actions/list-presets.md) | GET |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [List Enterprise Users](actions/list-enterprise-users.md) | GET |  |

### User Task Status

| Action | Method | Description |
| --- | --- | --- |
| [Set User Status](actions/set-user-status.md) | PUT |  |

