# <img src="https://images.mindcloud.co/apps/icons/frameio-v4_1773431215684.png" alt="Frame.io v4 logo" width="28" height="28"> Frame.io v4: Universal API

Review, share, and manage media projects and files

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/frameioV4/latest
- **Category:** Content & Files / Storage
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://frame.io/
- **Vendor API docs:** https://next.developer.frame.io/platform/api-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get User Details](actions/get-user-details.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/frameioV4/latest/actions/get-user-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [List Accounts](actions/list-accounts.md) | GET | Retrieves accounts from Frame.io v4. |

### Comments

| Action | Method | Description |
| --- | --- | --- |
| [Create Comment](actions/create-comment.md) | POST | Creates a new comment in Frame.io v4. |
| [Get Comment](actions/get-comment.md) | GET | Retrieves a comment from Frame.io v4. |
| [List Comments](actions/list-comments.md) | GET | Retrieves comments for a file in Frame.io v4. |
| [Update Comment](actions/update-comment.md) | PUT | Updates an existing comment in Frame.io v4. |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Copy File](actions/copy-file.md) | POST | Copies a file in Frame.io v4. |
| [Create File Local Upload](actions/create-file-local-upload.md) | POST | Creates a new file via local upload in Frame.io v4. |
| [Create File Remote Upload](actions/create-file-remote-upload.md) | POST | Creates a new file via remote upload in Frame.io v4. |
| [Get File](actions/get-file.md) | GET | Retrieves a file from Frame.io v4. |
| [Get File Upload Status](actions/get-file-upload-status.md) | GET | Retrieves file upload status from Frame.io v4. |
| [Import File](actions/import-file.md) | POST | Imports a file into Frame.io v4. |
| [List Files](actions/list-files.md) | GET | Retrieves files from a folder in Frame.io v4. |
| [Move File](actions/move-file.md) | PUT | Moves a file in Frame.io v4. |
| [Update File](actions/update-file.md) | PUT | Updates an existing file in Frame.io v4. |

### Folders

| Action | Method | Description |
| --- | --- | --- |
| [Copy Folder](actions/copy-folder.md) | POST | Copies a folder in Frame.io v4. |
| [Create Folder](actions/create-folder.md) | POST | Creates a new subfolder in Frame.io v4. |
| [Get Folder](actions/get-folder.md) | GET | Retrieves a folder from Frame.io v4. |
| [List Folder Children](actions/list-folder-children.md) | GET | Retrieves child items for a folder in Frame.io v4. |
| [List Folders](actions/list-folders.md) | GET | Retrieves subfolders from a folder in Frame.io v4. |
| [Move Folder](actions/move-folder.md) | PUT | Moves a folder in Frame.io v4. |
| [Update Folder](actions/update-folder.md) | PUT | Updates an existing folder in Frame.io v4. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a new project in Frame.io v4. |
| [Get Project](actions/get-project.md) | GET | Retrieves a project from Frame.io v4. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from a workspace in Frame.io v4. |
| [Update Project](actions/update-project.md) | PUT | Updates an existing project in Frame.io v4. |

### Share

| Action | Method | Description |
| --- | --- | --- |
| [Create Share](actions/create-share.md) | POST | Creates a new share in Frame.io v4. |
| [Get Share](actions/get-share.md) | GET | Retrieves a share from Frame.io v4. |
| [List Shares](actions/list-shares.md) | GET | Retrieves shares for a project in Frame.io v4. |
| [Update Share](actions/update-share.md) | PUT | Updates an existing share in Frame.io v4. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get User Details](actions/get-user-details.md) | GET | Retrieves the current user from Frame.io v4. |

### Version Stack

| Action | Method | Description |
| --- | --- | --- |
| [Copy Version Stack](actions/copy-version-stack.md) | POST | Copies a version stack in Frame.io v4. |
| [Create Version Stack](actions/create-version-stack.md) | POST | Creates a new version stack in Frame.io v4. |
| [Get Version Stack](actions/get-version-stack.md) | GET | Retrieves a version stack from Frame.io v4. |
| [List Version Stack Children](actions/list-version-stack-children.md) | GET | Retrieves child items for a version stack in Frame.io v4. |
| [List Version Stacks](actions/list-version-stacks.md) | GET | Retrieves version stacks from a folder in Frame.io v4. |
| [Move Version Stack](actions/move-version-stack.md) | PUT | Moves a version stack in Frame.io v4. |

### Workspaces

| Action | Method | Description |
| --- | --- | --- |
| [Create Workspace](actions/create-workspace.md) | POST | Creates a new workspace in Frame.io v4. |
| [Get Workspace](actions/get-workspace.md) | GET | Retrieves a workspace from Frame.io v4. |
| [List Workspaces](actions/list-workspaces.md) | GET | Retrieves workspaces from an account in Frame.io v4. |
| [Update Workspace](actions/update-workspace.md) | PUT | Updates an existing workspace in Frame.io v4. |

