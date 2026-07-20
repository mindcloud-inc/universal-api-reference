# <img src="https://images.mindcloud.co/apps/icons/logo-app-icon-1_1774720318704.png" alt="Cirra logo" width="28" height="28"> Cirra: Universal API

Chat with apps, reuse skills, create triggers, and automate work.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/cirra/latest
- **Category:** IT Operations / Integration & Automation
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://app.mindcloud.co

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Threads](actions/list-threads.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cirra/latest/actions/list-threads?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### App

| Action | Method | Description |
| --- | --- | --- |
| [Get User Apps](actions/get-user-apps.md) | GET | Retrieves connected app records from Cirra. |

### Connections

| Action | Method | Description |
| --- | --- | --- |
| [Delete Connection](actions/delete-connection.md) | DELETE | Deletes a Cirra connection by credential ID. |
| [List Connections](actions/list-connections.md) | GET | Retrieves Cirra connections for the authenticated user. |

### Member

| Action | Method | Description |
| --- | --- | --- |
| [Invite Members](actions/invite-members.md) | POST | Invites members to the authenticated Cirra company. |
| [List Members](actions/list-members.md) | GET | Retrieves company member records from Cirra. |
| [Remove Member](actions/remove-member.md) | DELETE | Deletes a Cirra member by user ID. |
| [Set Member Role](actions/set-member-role.md) | PUT | Updates a Cirra member role by user ID. |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Send Thread Message](actions/send-thread-message.md) | POST | Adds a message to a Cirra thread and starts a run. |

### Role

| Action | Method | Description |
| --- | --- | --- |
| [Create Role](actions/create-role.md) | POST | Creates a new role in Cirra. |
| [Delete Role](actions/delete-role.md) | DELETE | Deletes a role from Cirra by role ID. |
| [List Roles](actions/list-roles.md) | GET | Retrieves company role records from Cirra. |

### Role Permission

| Action | Method | Description |
| --- | --- | --- |
| [Set Global Role Permissions](actions/set-global-role-permissions.md) | PUT |  |
| [Set Role App Permissions](actions/set-role-app-permissions.md) | PUT |  |
| [Set Role Model Permissions](actions/set-role-model-permissions.md) | PUT |  |

### Role Permission Coverage

| Action | Method | Description |
| --- | --- | --- |
| [List Role App Permissions](actions/list-role-app-permissions.md) | GET |  |
| [List Role Model Permissions](actions/list-role-model-permissions.md) | GET |  |

### Settings

| Action | Method | Description |
| --- | --- | --- |
| [Get Settings](actions/get-settings.md) | GET | Retrieves synced user settings from Cirra. |
| [Update Settings](actions/update-settings.md) | PUT | Updates synced user settings in Cirra. |

### Thread

| Action | Method | Description |
| --- | --- | --- |
| [Archive Thread](actions/archive-thread.md) | PUT | Archives an existing Cirra thread by thread ID. |
| [Clear Thread Messages](actions/clear-thread-messages.md) | PUT | Clears all messages from a Cirra thread. |
| [Create Thread](actions/create-thread.md) | POST | Creates a Cirra thread and starts its initial run. |
| [List Threads](actions/list-threads.md) | GET | Retrieves Cirra threads for the authenticated user. |
| [Get Thread](actions/read-thread.md) | GET | Retrieves a Cirra thread by thread ID. |
| [Unarchive Thread](actions/unarchive-thread.md) | PUT | Restores an archived Cirra thread by thread ID. |

