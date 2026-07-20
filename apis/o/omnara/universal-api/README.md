# <img src="https://images.mindcloud.co/apps/icons/omnara_1775677798210.png" alt="Omnara logo" width="28" height="28"> Omnara: Universal API

Omnara is a coding-agent orchestration platform for managing users, sessions, workspaces, machines, and worktrees over a REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/omnara/latest
- **Actions:** 49
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://omnara.com
- **Vendor API docs:** https://docs.omnara.com/api-reference/overview

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User Profile](actions/get-current-user-profile.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/omnara/latest/actions/get-current-user-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (49)

### API Keys

| Action | Method | Description |
| --- | --- | --- |
| [Create PAT](actions/create-pat.md) | POST |  |
| [Delete PAT](actions/delete-pat.md) | DELETE |  |
| [List PATs](actions/list-pa-ts.md) | GET |  |

### Branches

| Action | Method | Description |
| --- | --- | --- |
| [Ensure Worktree](actions/ensure-worktree.md) | POST |  |
| [Get Worktree](actions/get-worktree.md) | GET |  |
| [Init Worktree Checkpoint](actions/init-worktree-checkpoint.md) | POST |  |
| [List Workspace Worktrees](actions/list-workspace-worktrees.md) | GET |  |
| [Migrate Worktree](actions/migrate-worktree.md) | PUT |  |

### Devices

| Action | Method | Description |
| --- | --- | --- |
| [List Machines](actions/list-machines.md) | GET |  |
| [Register Machine](actions/register-machine.md) | POST |  |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Check Base Ref Bundle Exists](actions/check-base-ref-bundle-exists.md) | GET |  |
| [Check Head Ref Bundle Exists](actions/check-head-ref-bundle-exists.md) | GET |  |
| [Get Base Ref Upload Url](actions/get-base-ref-upload-url.md) | POST |  |
| [Get Checkpoint Download Urls](actions/get-checkpoint-download-urls.md) | POST |  |
| [Get Checkpoint Upload Urls](actions/get-checkpoint-upload-urls.md) | POST |  |
| [Get Sync Download Url](actions/get-sync-download-url.md) | POST |  |
| [Get Sync Upload Url](actions/get-sync-upload-url.md) | POST |  |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Queued Message](actions/cancel-queued-message.md) | DELETE |  |
| [Get Agent Session Messages](actions/get-agent-session-messages.md) | GET |  |
| [Mark Agent Session Read](actions/mark-agent-session-read.md) | PUT |  |

### Sessions

| Action | Method | Description |
| --- | --- | --- |
| [Create User Session](actions/create-user-session.md) | POST |  |
| [Delete User Session](actions/delete-user-session.md) | DELETE |  |
| [Get Agent Session Detail](actions/get-agent-session-detail.md) | GET |  |
| [Get User Session Detail](actions/get-user-session-detail.md) | GET |  |
| [Import Claude Session](actions/import-claude-session.md) | POST |  |
| [Launch Workspace Session](actions/launch-workspace-session.md) | POST |  |
| [Refresh Relay Token](actions/refresh-relay-token.md) | PUT |  |
| [Register Relay Instance](actions/register-relay-instance.md) | POST |  |
| [Restart User Session](actions/restart-user-session.md) | PUT |  |
| [Set User Session Worktree](actions/set-user-session-worktree.md) | PUT |  |
| [Stop User Session](actions/stop-user-session.md) | PUT |  |
| [Update User Session](actions/update-user-session.md) | PUT |  |

### Sync States

| Action | Method | Description |
| --- | --- | --- |
| [Get Sync State](actions/get-sync-state.md) | GET |  |
| [List Sync Checkpoints](actions/list-sync-checkpoints.md) | GET |  |
| [Update Checkpoint Sync Status](actions/update-checkpoint-sync-status.md) | PUT |  |
| [Update Sync State](actions/update-sync-state.md) | PUT |  |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Get Full Settings](actions/get-full-settings.md) | GET |  |
| [Update User Settings](actions/update-user-settings.md) | PUT |  |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Delete User Account](actions/delete-user-account.md) | DELETE |  |
| [Get Current User Profile](actions/get-current-user-profile.md) | GET |  |
| [Get Session](actions/get-session.md) | GET |  |
| [Sync User](actions/sync-user.md) | PUT |  |
| [Update Current User Profile](actions/update-current-user-profile.md) | PUT |  |

### Workspaces

| Action | Method | Description |
| --- | --- | --- |
| [Delete Workspace](actions/delete-workspace.md) | DELETE |  |
| [Enable Workspace Sync](actions/enable-workspace-sync.md) | PUT |  |
| [Ensure Workspace](actions/ensure-workspace.md) | POST |  |
| [Get Workspace By Id](actions/get-workspace-by-id.md) | GET |  |
| [Get Workspace By Path](actions/get-workspace-by-path.md) | GET |  |
| [Update Workspace Config](actions/update-workspace-config.md) | PUT |  |

