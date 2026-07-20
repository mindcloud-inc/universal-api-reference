# CompanyCam: Native API Reference

A consolidated summary of CompanyCam's API configuration and 48 documented operations, with links to official documentation.

- **Official docs:** https://docs.companycam.com/reference/
- **OpenAPI specification:** https://github.com/CompanyCam/openapi-spec/blob/main/openapi.yaml
- **API base URL:** `https://api.companycam.com/v2/`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

### OAuth 2.0

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://app.companycam.com/oauth/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://app.companycam.com/oauth/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `read write destroy`.

Refresh expired access tokens with a POST request to https://app.companycam.com/oauth/token.

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

Responses from this API use JSON.

## Pagination

Use `per_page` in the query string to set the page size (default 25; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (48 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Comment to Project](actions/add-comment-to-project.md) | `POST projects/:id/comments` | [docs](https://docs.companycam.com/reference/createprojectcomment) |
| [Add Label to Project](actions/add-label-to-project.md) | `POST projects/:projectId/labels` | [docs](https://docs.companycam.com/reference/listprojects) |
| [Add Photo to Project](actions/add-photo-to-project.md) | `POST projects/:project_id/photos` | [docs](https://docs.companycam.com/reference/createprojectphoto) |
| [Add Tags to Photo](actions/add-tags-to-photo.md) | `POST photos/:id/tags` | [docs](https://docs.companycam.com/reference/listphototags) |
| [Add User to Project](actions/add-user-to-project.md) | `PUT projects/:projectId/assigned_users/:userId` | [docs](https://docs.companycam.com/reference/assignusertoproject) |
| [Archive Project](actions/archive-project.md) | `PATCH projects/:id/archive` | [docs](https://docs.companycam.com/reference/archiveproject) |
| [Create Group](actions/create-group.md) | `POST groups` | [docs](https://docs.companycam.com/reference/creategroup) |
| [Create Project](actions/create-project.md) | `POST projects` | [docs](https://docs.companycam.com/reference/createproject) |
| [Create User](actions/create-user.md) | `POST users` | [docs](https://docs.companycam.com/reference/createuser) |
| [Create Webhook](actions/create-webhook.md) | `POST webhooks` | [docs](https://docs.companycam.com/reference/createwebhook) |
| [Delete Group](actions/delete-group.md) | `DELETE groups/:id` | [docs](https://docs.companycam.com/reference/deletegroup) |
| [Delete Photo](actions/delete-photo.md) | `DELETE photos/:id` | [docs](https://docs.companycam.com/reference/updatephotodescription) |
| [Delete Project Label](actions/delete-project-label.md) | `GET projects/:id/labels/:labelId` | [docs](https://docs.companycam.com/reference/listprojectlabels) |
| [Delete User](actions/delete-user.md) | `DELETE users/:id` | [docs](https://docs.companycam.com/reference/getuser) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE webhooks/:id` | [docs](https://docs.companycam.com/reference/deletewebhook) |
| [Get Company](actions/get-company.md) | `GET company` | [docs](https://docs.companycam.com/reference/getcurrentcompany) |
| [Get Current User](actions/get-current-user.md) | `GET users/current` | [docs](https://docs.companycam.com/reference/getcurrentuser) |
| [Get Group](actions/get-group.md) | `GET groups/:id` | [docs](https://docs.companycam.com/reference/getgroup) |
| [Get Photo](actions/get-photo.md) | `GET photos/:id` | [docs](https://docs.companycam.com/reference/getphoto) |
| [Get Project](actions/get-project.md) | `GET projects/:projectId` | [docs](https://docs.companycam.com/reference/getproject) |
| [Get Project Checklist](actions/get-project-checklist.md) | `GET projects/:projectId/checklists/:checklistId` | [docs](https://docs.companycam.com/reference/getprojectchecklist) |
| [Get User](actions/get-user.md) | `GET users/:id` | [docs](https://docs.companycam.com/reference/getuser) |
| [Get Video](actions/get-video.md) | `GET videos/:id` | [docs](https://docs.companycam.com/reference/getvideo) |
| [Get Webhook](actions/get-webhook.md) | `GET webhooks/:id` | [docs](https://docs.companycam.com/reference/getwebhook) |
| [List All Checklists](actions/list-all-checklists.md) | `GET checklists` | [docs](https://docs.companycam.com/reference/listchecklists) |
| [List Photo Comments](actions/list-photo-comments.md) | `GET photos/:id/comments` | [docs](https://docs.companycam.com/reference/listphotocomments) |
| [List Photo Tags](actions/list-photo-tags.md) | `GET photos/:id/tags` | [docs](https://docs.companycam.com/reference/listphototags) |
| [List Photos](actions/list-photos.md) | `GET photos` | [docs](https://docs.companycam.com/reference/listphotos) |
| [List Project Checklists](actions/list-project-checklists.md) | `GET projects/:projectId/checklists` | [docs](https://docs.companycam.com/reference/listprojectchecklists) |
| [List Project Comments](actions/list-project-comments.md) | `GET projects/:id/comments` | [docs](https://docs.companycam.com/reference/listprojectcomments) |
| [List Project Documents](actions/list-project-documents.md) | `GET projects/:projectId/documents` | [docs](https://docs.companycam.com/reference/listprojectdocuments) |
| [List Project Photos](actions/list-project-photos.md) | `GET projects/:projectId/photos` | [docs](https://docs.companycam.com/reference/listprojectphotos) |
| [List Project Users](actions/list-project-users.md) | `GET projects/:id/assigned_users` | [docs](https://docs.companycam.com/reference/listprojectassignedusers) |
| [List Project Videos](actions/list-project-videos.md) | `GET projects/:projectId/videos` | [docs](https://docs.companycam.com/reference/listprojectvideos) |
| [List Projects](actions/list-projects.md) | `GET projects` | [docs](https://docs.companycam.com/reference/listprojects) |
| [List Tags](actions/list-tags.md) | `GET tags` | [docs](https://docs.companycam.com/reference/listtags) |
| [List Users](actions/list-users.md) | `GET users` | [docs](https://docs.companycam.com/reference/listusers) |
| [List Videos](actions/list-videos.md) | `GET videos` | [docs](https://docs.companycam.com/reference/listvideos) |
| [List Webhooks](actions/list-webhooks.md) | `GET webhooks` | [docs](https://docs.companycam.com/reference/listwebhooks) |
| [Delete Project](actions/new-action1.md) | `DELETE https://api.companycam.com/v2/projects/:id` | [docs](https://docs.companycam.com/reference/deleteproject) |
| [Remove User from Project](actions/remove-user-from-project.md) | `DELETE projects/:id/assigned_users/:userId` | [docs](https://docs.companycam.com/reference/removeuserfromproject) |
| [Update Group](actions/update-group.md) | `PUT groups/:id` | [docs](https://docs.companycam.com/reference/updategroup) |
| [Update Photo](actions/update-photo.md) | `PUT photos/:id` | [docs](https://docs.companycam.com/reference/updatephotodescription) |
| [Update Photo Description](actions/update-photo-description.md) | `POST photos/:id/descriptions` | [docs](https://docs.companycam.com/reference/updatephotodescription) |
| [Update Project](actions/update-project.md) | `PUT projects/:id` | [docs](https://docs.companycam.com/reference/updateproject) |
| [Update User](actions/update-user.md) | `PUT users/:id` | [docs](https://docs.companycam.com/reference/updateuser) |
| [Update Webhook](actions/update-webhook.md) | `PUT webhooks/:id` | [docs](https://docs.companycam.com/reference/updatewebhook) |
| [Upload Project Document](actions/upload-project-document.md) | `POST projects/:projectId/documents` | [docs](https://docs.companycam.com/reference/listprojectdocuments) |
