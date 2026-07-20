# Omnara: Native API Reference

A consolidated summary of Omnara's API configuration and 49 documented operations, with links to official documentation.

- **Official docs:** https://docs.omnara.com/api-reference/overview
- **API base URL:** `https://api.omnara.com`

## Authentication

### Personal Access Token

Use an Omnara personal access token (PAT). Omnara requires Authorization: Bearer <token> on API requests.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.omnara.com/api-reference/overview)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (49 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Queued Message](actions/cancel-queued-message.md) | `DELETE /api/v1/user-sessions/{userSessionId}/agent-sessions/{agentSessionId}/messages/{messageId}` | [docs](https://docs.omnara.com/api-reference/user_sessions/cancel-queued-message) |
| [Check Base Ref Bundle Exists](actions/check-base-ref-bundle-exists.md) | `POST /api/v1/workspaces/{workspaceId}/sync/base-ref-exists` | [docs](https://docs.omnara.com/api-reference/workspaces/check-base-ref-bundle-exists) |
| [Check Head Ref Bundle Exists](actions/check-head-ref-bundle-exists.md) | `POST /api/v1/workspaces/{workspaceId}/sync/head-ref-exists` | [docs](https://docs.omnara.com/api-reference/workspaces/check-head-ref-bundle-exists) |
| [Create PAT](actions/create-pat.md) | `POST /api/v1/auth/pat` | [docs](https://docs.omnara.com/api-reference/auth/create-pat) |
| [Create User Session](actions/create-user-session.md) | `POST /api/v1/user-sessions` | [docs](https://docs.omnara.com/api-reference/user_sessions/create-user-session-endpoint) |
| [Delete PAT](actions/delete-pat.md) | `DELETE /api/v1/auth/pat/{patId}` | [docs](https://docs.omnara.com/api-reference/auth/delete-pat) |
| [Delete User Account](actions/delete-user-account.md) | `DELETE /api/v1/auth/me` | [docs](https://docs.omnara.com/api-reference/auth/delete-user-account) |
| [Delete User Session](actions/delete-user-session.md) | `DELETE /api/v1/user-sessions/{userSessionId}` | [docs](https://docs.omnara.com/api-reference/user_sessions/delete-user-session) |
| [Delete Workspace](actions/delete-workspace.md) | `DELETE /api/v1/workspaces/{workspaceId}` | [docs](https://docs.omnara.com/api-reference/workspaces/delete-workspace) |
| [Enable Workspace Sync](actions/enable-workspace-sync.md) | `POST /api/v1/workspaces/{workspaceId}/sync/enable` | [docs](https://docs.omnara.com/api-reference/workspaces/enable-workspace-sync) |
| [Ensure Workspace](actions/ensure-workspace.md) | `POST /api/v1/workspaces/ensure` | [docs](https://docs.omnara.com/api-reference/workspaces/ensure-workspace) |
| [Ensure Worktree](actions/ensure-worktree.md) | `POST /api/v1/worktrees/ensure` | [docs](https://docs.omnara.com/api-reference/worktrees/ensure-worktree-endpoint) |
| [Get Agent Session Detail](actions/get-agent-session-detail.md) | `GET /api/v1/user-sessions/{userSessionId}/agent-sessions/{agentSessionId}` | [docs](https://docs.omnara.com/api-reference/user_sessions/get-agent-session-detail) |
| [Get Agent Session Messages](actions/get-agent-session-messages.md) | `GET /api/v1/user-sessions/{userSessionId}/agent-sessions/{agentSessionId}/messages` | [docs](https://docs.omnara.com/api-reference/user_sessions/get-agent-session-messages) |
| [Get Base Ref Upload Url](actions/get-base-ref-upload-url.md) | `POST /api/v1/workspaces/{workspaceId}/sync/base-ref-upload-url` | [docs](https://docs.omnara.com/api-reference/workspaces/get-base-ref-upload-url) |
| [Get Checkpoint Download Urls](actions/get-checkpoint-download-urls.md) | `POST /api/v1/workspaces/{workspaceId}/sync/checkpoint-download-url` | [docs](https://docs.omnara.com/api-reference/workspaces/get-checkpoint-download-urls) |
| [Get Checkpoint Upload Urls](actions/get-checkpoint-upload-urls.md) | `POST /api/v1/workspaces/{workspaceId}/sync/checkpoint-upload-url` | [docs](https://docs.omnara.com/api-reference/workspaces/get-checkpoint-upload-urls) |
| [Get Current User Profile](actions/get-current-user-profile.md) | `GET /api/v1/auth/me` | [docs](https://docs.omnara.com/api-reference/auth/get-current-user-profile) |
| [Get Full Settings](actions/get-full-settings.md) | `GET /api/v1/user/settings` | [docs](https://docs.omnara.com/api-reference/user-settings/get-full-settings) |
| [Get Session](actions/get-session.md) | `GET /api/v1/auth/session` | [docs](https://docs.omnara.com/api-reference/auth/get-session) |
| [Get Sync Download Url](actions/get-sync-download-url.md) | `POST /api/v1/workspaces/{workspaceId}/sync/download-url` | [docs](https://docs.omnara.com/api-reference/workspaces/get-sync-download-url) |
| [Get Sync State](actions/get-sync-state.md) | `GET /api/v1/workspaces/{workspaceId}/sync/state` | [docs](https://docs.omnara.com/api-reference/workspaces/get-sync-state) |
| [Get Sync Upload Url](actions/get-sync-upload-url.md) | `POST /api/v1/workspaces/{workspaceId}/sync/upload-url` | [docs](https://docs.omnara.com/api-reference/workspaces/get-sync-upload-url) |
| [Get User Session Detail](actions/get-user-session-detail.md) | `GET /api/v1/user-sessions/{userSessionId}` | [docs](https://docs.omnara.com/api-reference/user_sessions/get-user-session-detail) |
| [Get Workspace By Id](actions/get-workspace-by-id.md) | `GET /api/v1/workspaces/{workspaceId}` | [docs](https://docs.omnara.com/api-reference/workspaces/get-workspace-by-id) |
| [Get Workspace By Path](actions/get-workspace-by-path.md) | `GET /api/v1/workspaces/by-path` | [docs](https://docs.omnara.com/api-reference/workspaces/get-workspace-by-path) |
| [Get Worktree](actions/get-worktree.md) | `GET /api/v1/worktrees/{worktreeId}` | [docs](https://docs.omnara.com/api-reference/worktrees/get-worktree-endpoint) |
| [Import Claude Session](actions/import-claude-session.md) | `POST /api/v1/user-sessions/import-claude-session` | [docs](https://docs.omnara.com/api-reference/user_sessions/import-claude-session) |
| [Init Worktree Checkpoint](actions/init-worktree-checkpoint.md) | `POST /api/v1/workspaces/{workspaceId}/sync/init-worktree-checkpoint` | [docs](https://docs.omnara.com/api-reference/workspaces/init-worktree-checkpoint) |
| [Launch Workspace Session](actions/launch-workspace-session.md) | `POST /api/v1/workspaces/{workspaceId}/sessions` | [docs](https://docs.omnara.com/api-reference/workspaces/launch-workspace-session) |
| [List Machines](actions/list-machines.md) | `GET /api/v1/machines` | [docs](https://docs.omnara.com/api-reference/machines/list-machines) |
| [List PATs](actions/list-pa-ts.md) | `GET /api/v1/auth/pat` | [docs](https://docs.omnara.com/api-reference/auth/list-pats) |
| [List Sync Checkpoints](actions/list-sync-checkpoints.md) | `GET /api/v1/workspaces/{workspaceId}/sync/checkpoints` | [docs](https://docs.omnara.com/api-reference/workspaces/list-sync-checkpoints) |
| [List Workspace Worktrees](actions/list-workspace-worktrees.md) | `GET /api/v1/worktrees/workspace/{workspaceId}` | [docs](https://docs.omnara.com/api-reference/worktrees/list-workspace-worktrees) |
| [Mark Agent Session Read](actions/mark-agent-session-read.md) | `POST /api/v1/user-sessions/{userSessionId}/agent-sessions/{agentSessionId}/mark-read` | [docs](https://docs.omnara.com/api-reference/user_sessions/mark-agent-session-read) |
| [Migrate Worktree](actions/migrate-worktree.md) | `POST /api/v1/worktrees/{worktreeId}/migrate` | [docs](https://docs.omnara.com/api-reference/worktrees/migrate-worktree) |
| [Refresh Relay Token](actions/refresh-relay-token.md) | `POST /api/v1/relay/refresh` | [docs](https://docs.omnara.com/api-reference/relay/refresh-relay-token) |
| [Register Machine](actions/register-machine.md) | `POST /api/v1/machines/register` | [docs](https://docs.omnara.com/api-reference/machines/register-machine) |
| [Register Relay Instance](actions/register-relay-instance.md) | `POST /api/v1/relay/register` | [docs](https://docs.omnara.com/api-reference/relay/register-relay-instance) |
| [Restart User Session](actions/restart-user-session.md) | `POST /api/v1/user-sessions/{userSessionId}/restart` | [docs](https://docs.omnara.com/api-reference/user_sessions/restart-user-session) |
| [Set User Session Worktree](actions/set-user-session-worktree.md) | `PATCH /api/v1/worktrees/session/{sessionId}` | [docs](https://docs.omnara.com/api-reference/worktrees/set-user-session-worktree) |
| [Stop User Session](actions/stop-user-session.md) | `POST /api/v1/user-sessions/{userSessionId}/stop` | [docs](https://docs.omnara.com/api-reference/user_sessions/stop-user-session) |
| [Sync User](actions/sync-user.md) | `POST /api/v1/auth/sync-user` | [docs](https://docs.omnara.com/api-reference/auth/sync-user) |
| [Update Checkpoint Sync Status](actions/update-checkpoint-sync-status.md) | `PATCH /api/v1/workspaces/{workspaceId}/sync/checkpoint-status` | [docs](https://docs.omnara.com/api-reference/workspaces/update-checkpoint-sync-status) |
| [Update Current User Profile](actions/update-current-user-profile.md) | `PATCH /api/v1/auth/me` | [docs](https://docs.omnara.com/api-reference/auth/update-current-user-profile) |
| [Update Sync State](actions/update-sync-state.md) | `PATCH /api/v1/workspaces/{workspaceId}/sync/state` | [docs](https://docs.omnara.com/api-reference/workspaces/update-sync-state) |
| [Update User Session](actions/update-user-session.md) | `PATCH /api/v1/user-sessions/{userSessionId}` | [docs](https://docs.omnara.com/api-reference/user_sessions/update-user-session) |
| [Update User Settings](actions/update-user-settings.md) | `PATCH /api/v1/user/settings` | [docs](https://docs.omnara.com/api-reference/user-settings/update-user-settings) |
| [Update Workspace Config](actions/update-workspace-config.md) | `PATCH /api/v1/workspaces/{workspaceId}/config` | [docs](https://docs.omnara.com/api-reference/workspaces/update-workspace-config) |
