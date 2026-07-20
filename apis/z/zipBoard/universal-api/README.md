# <img src="https://images.mindcloud.co/apps/icons/zipboard-sqaure-logo_1775073442459.png" alt="zipBoard logo" width="28" height="28"> zipBoard: Universal API

Visual collaboration and review platform for collecting feedback, managing projects and files, sharing review links, and tracking issues across digital assets.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/zipBoard/latest
- **Category:** Productivity / Project Management
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://zipboard.co
- **Vendor API docs:** https://docs.zipboard.co/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Organizations](actions/get-organizations.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zipBoard/latest/actions/get-organizations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Comments

| Action | Method | Description |
| --- | --- | --- |
| [Create Feedback](actions/create-feedback.md) | POST | Creates a new feedback comment in zipBoard. |
| [Create Response](actions/create-response.md) | POST | Creates a new response in zipBoard. |
| [Delete Feedback](actions/delete-feedback.md) | DELETE | Deletes an existing feedback comment from zipBoard. |
| [Delete Response](actions/delete-response.md) | DELETE | Deletes an existing response from zipBoard. |
| [Get Feedback](actions/get-feedback.md) | GET | Retrieves feedback comments from zipBoard. |
| [Get Responses](actions/get-responses.md) | GET | Retrieves responses from zipBoard. |
| [Update Feedback](actions/update-feedback.md) | PUT | Updates an existing feedback comment in zipBoard. |
| [Update Response](actions/update-response.md) | PUT | Updates an existing response in zipBoard. |

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization](actions/get-organization.md) | GET | Retrieves organization details from zipBoard. |
| [Get Organizations](actions/get-organizations.md) | GET | Retrieves organizations from zipBoard. |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Create File](actions/create-file.md) | POST | Creates a new file in zipBoard. |
| [Create Review Link](actions/create-review-link.md) | POST | Creates a new review link in zipBoard. |
| [Delete File](actions/delete-file.md) | DELETE | Deletes an existing file from zipBoard. |
| [Delete Review Link](actions/delete-review-link.md) | DELETE | Deletes an existing review link from zipBoard. |
| [Get Files](actions/get-files.md) | GET | Retrieves files from zipBoard. |
| [Get Review Links](actions/get-review-links.md) | GET | Retrieves review links from zipBoard. |
| [Update File](actions/update-file.md) | PUT | Updates an existing file in zipBoard. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a new project in zipBoard. |
| [Delete Project](actions/delete-project.md) | DELETE | Deletes an existing project from zipBoard. |
| [Get Projects](actions/get-projects.md) | GET | Retrieves projects from zipBoard. |
| [Update Project](actions/update-project.md) | PUT | Updates an existing project in zipBoard. |

### Tickets

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST | Creates a new task in zipBoard. |
| [Delete Task](actions/delete-task.md) | DELETE | Deletes an existing task from zipBoard. |
| [Get Tasks](actions/get-tasks.md) | GET | Retrieves tasks from zipBoard. |
| [Update Task](actions/update-task.md) | PUT | Updates an existing task in zipBoard. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Project Collaborators](actions/get-project-collaborators.md) | GET | Retrieves project collaborators from zipBoard. |
| [Get User](actions/get-user.md) | GET | Retrieves user details from zipBoard. |
| [Get User by ID](actions/get-user-by-id.md) | GET | Retrieves a user by ID from zipBoard. |
| [Remove Project Collaborator](actions/remove-project-collaborator.md) | DELETE | Removes a project collaborator from zipBoard. |
| [Update User](actions/update-user.md) | PUT | Updates an existing user in zipBoard. |

