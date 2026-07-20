# <img src="https://images.mindcloud.co/apps/icons/viqeo_1775150601526.png" alt="Viqeo logo" width="28" height="28"> Viqeo: Universal API

Create, edit, and manage Viqeo projects, users, and stories

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/viqeo/latest
- **Category:** Communication / Video Communications
- **Actions:** 15
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://viqeo.tv
- **Vendor API docs:** https://support.viqeo.tv/en/articles/8962790-media-editor-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Projects](actions/list-projects.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/viqeo/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (15)

### Editor Session

| Action | Method | Description |
| --- | --- | --- |
| [Authenticate Project User](actions/authenticate-project-user.md) | POST | Authenticates a project user in Viqeo. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a new project in Viqeo. |
| [Delete Project](actions/delete-project.md) | DELETE | Deletes an existing project from Viqeo. |
| [Get Project](actions/get-project.md) | GET | Retrieves a project record from Viqeo. |
| [List Projects](actions/list-projects.md) | GET | Retrieves all project records from Viqeo. |
| [Update Project](actions/update-project.md) | PUT | Updates an existing project in Viqeo. |

### Story

| Action | Method | Description |
| --- | --- | --- |
| [Create Story](actions/create-story.md) | POST | Creates a new story in Viqeo. |
| [Delete Story](actions/delete-story.md) | DELETE | Deletes an existing story from Viqeo. |
| [Get Story](actions/get-story.md) | GET | Retrieves a story record from Viqeo. |
| [List Stories](actions/list-stories.md) | GET | Retrieves all story records from Viqeo. |
| [Update Story](actions/update-story.md) | PUT | Updates an existing story in Viqeo. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Create Project User](actions/create-project-user.md) | POST | Creates a new project user in Viqeo. |
| [Delete Project User](actions/delete-project-user.md) | DELETE | Deletes an existing project user from Viqeo. |
| [Get Project User](actions/get-project-user.md) | GET | Retrieves a project user from Viqeo. |
| [List Project Users](actions/list-project-users.md) | GET | Retrieves all project users from Viqeo. |

