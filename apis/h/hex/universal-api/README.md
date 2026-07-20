# <img src="https://images.mindcloud.co/apps/icons/hex-icon_1775576355519.png" alt="Hex logo" width="28" height="28"> Hex: Universal API

Manage Hex projects, runs, sharing, groups, and collections

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/hex/latest
- **Category:** Business Intelligence / Analytics & BI
- **Actions:** 19
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://hex.tech
- **Vendor API docs:** https://learn.hex.tech/docs/api-integrations/api/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Projects](actions/list-projects.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hex/latest/actions/list-projects?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (19)

### Collection

| Action | Method | Description |
| --- | --- | --- |
| [Create Collection](actions/create-collection.md) | POST |  |
| [Get Collection](actions/get-collection.md) | GET |  |
| [List Collections](actions/list-collections.md) | GET |  |
| [Update Collection](actions/update-collection.md) | PUT |  |

### Group

| Action | Method | Description |
| --- | --- | --- |
| [Create Group](actions/create-group.md) | POST |  |
| [Delete Group](actions/delete-group.md) | DELETE |  |
| [Get Group](actions/get-group.md) | GET |  |
| [List Groups](actions/list-groups.md) | GET |  |
| [Update Group](actions/update-group.md) | PUT |  |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Project Run](actions/cancel-project-run.md) | DELETE |  |
| [Create Presigned Embed URL](actions/create-presigned-embed-url.md) | POST |  |
| [Create Project](actions/create-project.md) | POST |  |
| [Get Project](actions/get-project.md) | GET |  |
| [Get Project Run](actions/get-project-run.md) | GET |  |
| [List Project Runs](actions/list-project-runs.md) | GET |  |
| [List Projects](actions/list-projects.md) | GET |  |
| [Run Project](actions/run-project.md) | POST |  |
| [Update Project](actions/update-project.md) | PUT |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [List Users](actions/list-users.md) | GET |  |

