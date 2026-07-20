# <img src="https://images.mindcloud.co/apps/icons/favicon-docs-browser-use-com-48x48_1777482257185.png" alt="Browser Use logo" width="28" height="28"> Browser Use: Universal API

Browser Use provides managed AI browser automation, persistent browser sessions, profiles, workspaces, files, and account billing APIs.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/browserUse/latest
- **Actions:** 25
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://browser-use.com
- **Vendor API docs:** https://docs.browser-use.com/cloud/api-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account Billing](actions/get-account-billing.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/browserUse/latest/actions/get-account-billing?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (25)

### Account Billing

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Billing](actions/get-account-billing.md) | GET | Retrieves account billing details from Browser Use. |

### Browser Session

| Action | Method | Description |
| --- | --- | --- |
| [Create Browser Session](actions/create-browser-session.md) | POST | Creates a browser session in Browser Use. |
| [Get Browser Session](actions/get-browser-session.md) | GET | Retrieves a browser session from Browser Use. |
| [List Browser Sessions](actions/list-browser-sessions.md) | GET | Retrieves browser sessions from Browser Use. |
| [Stop Browser Session](actions/stop-browser-session.md) | PUT | Stops a browser session in Browser Use. |

### Profile

| Action | Method | Description |
| --- | --- | --- |
| [Create Profile](actions/create-profile.md) | POST | Creates a profile in Browser Use. |
| [Delete Profile](actions/delete-profile.md) | DELETE | Deletes an existing profile from Browser Use. |
| [Get Profile](actions/get-profile.md) | GET | Retrieves a profile from Browser Use. |
| [List Profiles](actions/list-profiles.md) | GET | Retrieves profiles from Browser Use. |
| [Update Profile](actions/update-profile.md) | PUT | Updates an existing profile in Browser Use. |

### Session

| Action | Method | Description |
| --- | --- | --- |
| [Create Session](actions/create-session.md) | POST | Creates a session or dispatches a task in Browser Use. |
| [Delete Session](actions/delete-session.md) | DELETE | Deletes an existing session from Browser Use. |
| [Get Session](actions/get-session.md) | GET | Retrieves a session from Browser Use. |
| [List Sessions](actions/list-sessions.md) | GET | Retrieves sessions from Browser Use. |
| [Stop Session](actions/stop-session.md) | PUT | Stops a session or running task in Browser Use. |

### Session Message

| Action | Method | Description |
| --- | --- | --- |
| [List Session Messages](actions/list-session-messages.md) | GET | Retrieves session messages from Browser Use. |

### Workspace

| Action | Method | Description |
| --- | --- | --- |
| [Create Workspace](actions/create-workspace.md) | POST | Creates a workspace in Browser Use. |
| [Delete Workspace](actions/delete-workspace.md) | DELETE | Deletes an existing workspace from Browser Use. |
| [Get Workspace](actions/get-workspace.md) | GET | Retrieves a workspace from Browser Use. |
| [List Workspaces](actions/list-workspaces.md) | GET | Retrieves workspaces from Browser Use. |
| [Update Workspace](actions/update-workspace.md) | PUT | Updates an existing workspace in Browser Use. |

### Workspace File

| Action | Method | Description |
| --- | --- | --- |
| [Delete Workspace File](actions/delete-workspace-file.md) | DELETE | Deletes a workspace file from Browser Use. |
| [List Workspace Files](actions/list-workspace-files.md) | GET | Retrieves workspace files from Browser Use. |

### Workspace File Upload Url

| Action | Method | Description |
| --- | --- | --- |
| [Create Workspace File Upload URLs](actions/create-workspace-file-upload-urls.md) | POST | Retrieves presigned upload URLs for workspace files from Browser Use. |

### Workspace Size

| Action | Method | Description |
| --- | --- | --- |
| [Get Workspace Size](actions/get-workspace-size.md) | GET | Retrieves workspace storage usage from Browser Use. |

