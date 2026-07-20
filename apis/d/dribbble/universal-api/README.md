# <img src="https://images.mindcloud.co/apps/icons/dribbble_1775768266470.png" alt="Dribbble logo" width="28" height="28"> Dribbble: Universal API

Manage Dribbble profile, shots, projects, attachments, and jobs

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/dribbble/latest
- **Category:** Marketing / Social Media
- **Actions:** 15
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://dribbble.com
- **Vendor API docs:** https://developer.dribbble.com/v2/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dribbble/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (15)

### Attachment

| Action | Method | Description |
| --- | --- | --- |
| [Create Shot Attachment](actions/create-shot-attachment.md) | POST |  |
| [Delete Shot Attachment](actions/delete-shot-attachment.md) | DELETE |  |

### Job

| Action | Method | Description |
| --- | --- | --- |
| [Create Job](actions/create-job.md) | POST |  |
| [Get Job](actions/get-job.md) | GET |  |
| [Update Job](actions/update-job.md) | PUT |  |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST |  |
| [Delete Project](actions/delete-project.md) | DELETE |  |
| [List User Projects](actions/list-user-projects.md) | GET |  |
| [Update Project](actions/update-project.md) | PUT |  |

### Shot

| Action | Method | Description |
| --- | --- | --- |
| [Create Shot](actions/create-shot.md) | POST |  |
| [Delete Shot](actions/delete-shot.md) | DELETE |  |
| [Get Shot](actions/get-shot.md) | GET |  |
| [List User Shots](actions/list-user-shots.md) | GET |  |
| [Update Shot](actions/update-shot.md) | PUT |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET |  |

