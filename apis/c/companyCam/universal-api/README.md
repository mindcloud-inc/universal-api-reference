# <img src="https://images.mindcloud.co/apps/icons/company-cam-icon_1782393138406.png" alt="CompanyCam logo" width="28" height="28"> CompanyCam: Universal API

Job site photo tools to manage work from anywhere.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/companyCam/latest
- **Category:** Support / Field Service
- **Actions:** 52
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://companycam.com/
- **Vendor API docs:** https://docs.companycam.com/reference/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Company](actions/get-company.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/companyCam/latest/actions/get-company?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (52)

### Checklists

| Action | Method | Description |
| --- | --- | --- |
| [Get Project Checklist](actions/get-project-checklist.md) | GET | Retrieves a project checklist from CompanyCam. |
| [List All Checklists](actions/list-all-checklists.md) | GET | Retrieves a list of checklists from CompanyCam. |
| [List Project Checklists](actions/list-project-checklists.md) | GET | Retrieve all checklists for a CompanyCam project. |

### Comments

| Action | Method | Description |
| --- | --- | --- |
| [Add Comment to Photo](actions/add-comment-to-photo.md) | POST |  |
| [Add Comment to Project](actions/add-comment-to-project.md) | POST |  |
| [List Photo Comments](actions/list-photo-comments.md) | GET |  |
| [List Project Comments](actions/list-project-comments.md) | GET |  |

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Get Company](actions/get-company.md) | GET | Retrieves the current company from CompanyCam. |

### Document

| Action | Method | Description |
| --- | --- | --- |
| [List Project Documents](actions/list-project-documents.md) | GET | Retrieves documents from a CompanyCam project. |
| [Upload Project Document](actions/upload-project-document.md) | POST | Upload a document to a CompanyCam project. |

### Groups

| Action | Method | Description |
| --- | --- | --- |
| [Create Group](actions/create-group.md) | POST |  |
| [Delete Group](actions/delete-group.md) | DELETE |  |
| [Get Group](actions/get-group.md) | GET |  |
| [List Groups](actions/list-groups.md) | GET |  |
| [Update Group](actions/update-group.md) | PUT |  |

### Labels

| Action | Method | Description |
| --- | --- | --- |
| [Add Label to Project](actions/add-label-to-project.md) | POST |  |
| [Delete Project Label](actions/delete-project-label.md) | DELETE | Delete a label from a project by id. |
| [List Project Labels](actions/list-project-labels.md) | GET |  |

### Photo

| Action | Method | Description |
| --- | --- | --- |
| [Add Photo to Project](actions/add-photo-to-project.md) | POST | Adds a photo to a CompanyCam project. |
| [Delete Photo](actions/delete-photo.md) | DELETE |  |
| [Get Photo](actions/get-photo.md) | GET |  |
| [List Photos](actions/list-photos.md) | GET | Retrieves a list of photos from CompanyCam. |
| [List Project Photos](actions/list-project-photos.md) | GET |  |
| [Update Photo](actions/update-photo.md) | PUT |  |
| [Update Photo Description](actions/update-photo-description.md) | PUT |  |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Delete Project](actions/delete-project.md) | DELETE | Deletes an existing project from CompanyCam. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Archive Project](actions/archive-project.md) | PUT |  |
| [Create Project](actions/create-project.md) | POST | Creates a new project in CompanyCam. |
| [Get Project](actions/get-project.md) | GET | Retrieves an existing project from CompanyCam. |
| [List Projects](actions/list-projects.md) | GET | Retrieves a list of projects from CompanyCam. |
| [Update Project](actions/update-project.md) | PUT |  |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [Add Tags to Photo](actions/add-tags-to-photo.md) | PUT |  |
| [List Photo Tags](actions/list-photo-tags.md) | GET |  |
| [List Tags](actions/list-tags.md) | GET |  |

### Templates

| Action | Method | Description |
| --- | --- | --- |
| [List All Checklist Templates](actions/list-all-checklist-templates.md) | GET |  |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Add User to Project](actions/add-user-to-project.md) | POST | Assign a user to a project. |
| [Create User](actions/create-user.md) | POST | Create a new user in CompanyCam. |
| [Delete User](actions/delete-user.md) | DELETE | Delete an existing user from CompanyCam. |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the currently authenticated user from CompanyCam. |
| [Get User](actions/get-user.md) | GET | Retrieves an existing user from CompanyCam. |
| [List Project Users](actions/list-project-users.md) | GET | Retrieve a list of users assigned to a specified Project. |
| [List Users](actions/list-users.md) | GET |  |
| [Remove User from Project](actions/remove-user-from-project.md) | DELETE | Remove an assigned user from a specified Project. |
| [Update User](actions/update-user.md) | POST | Update an existing user in CompanyCam. |

### Video

| Action | Method | Description |
| --- | --- | --- |
| [Get Video](actions/get-video.md) | GET | Returns details for a single video. |
| [List Project Videos](actions/list-project-videos.md) | GET | Retrieve videos captured at a specified project. |
| [List Videos](actions/list-videos.md) | GET | Returns videos visible to the authenticated user, sorted by capture date (most recent first). |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in CompanyCam. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes an existing webhook from CompanyCam. |
| [Get Webhook](actions/get-webhook.md) | GET | Retrieves an existing webhook from CompanyCam. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves a list of webhooks from CompanyCam. |
| [Update Webhook](actions/update-webhook.md) | PUT | Updates an existing webhook in CompanyCam. |

