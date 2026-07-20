# <img src="https://images.mindcloud.co/apps/icons/codemagic_1776171947077.png" alt="Codemagic logo" width="28" height="28"> Codemagic: Universal API

Codemagic is a CI/CD platform for managing mobile and app builds, app previews, tester groups, variable groups, team resources, and over-the-air update metadata through its REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/codemagic/latest
- **Category:** IT Operations / DevOps
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://codemagic.io
- **Vendor API docs:** https://codemagic.io/api/v3/schema

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Authenticated User](actions/get-authenticated-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/codemagic/latest/actions/get-authenticated-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Actions

| Action | Method | Description |
| --- | --- | --- |
| [Get Build Actions](actions/get-build-actions.md) | GET | Retrieves actions for a specific Codemagic build. |

### Applications

| Action | Method | Description |
| --- | --- | --- |
| [Get App Preview](actions/get-app-preview.md) | GET | Retrieves a specific app preview from Codemagic. |
| [Get Shared App Preview](actions/get-shared-app-preview.md) | GET | Retrieves a shared app preview from Codemagic. |
| [List Authenticated User Apps](actions/list-authenticated-user-apps.md) | GET | Retrieves apps for the authenticated Codemagic user. |
| [List Team App Previews](actions/list-team-app-previews.md) | GET | Retrieves app previews for a specific Codemagic team. |
| [List Team Apps](actions/list-team-apps.md) | GET | Retrieves apps for a specific Codemagic team. |
| [Share App Preview](actions/share-app-preview.md) | POST | Creates a shared link for a Codemagic app preview. |
| [Start App Preview](actions/start-app-preview.md) | POST | Creates a new app preview for a Codemagic build. |
| [Stop App Preview](actions/stop-app-preview.md) | DELETE | Deletes an existing app preview from Codemagic. |

### Builds

| Action | Method | Description |
| --- | --- | --- |
| [Get Build](actions/get-build.md) | GET | Retrieves a specific build from Codemagic. |
| [List Team Builds](actions/list-team-builds.md) | GET | Retrieves builds for a specific Codemagic team. |

### Connections

| Action | Method | Description |
| --- | --- | --- |
| [Get Build Remote Access](actions/get-build-remote-access.md) | GET | Retrieves remote access details for a Codemagic build. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Import Tester Group Contacts](actions/bulk-import-tester-group-contacts.md) | POST | Bulk imports contacts into a Codemagic tester group. |
| [Delete Tester Group Contact](actions/delete-tester-group-contact.md) | DELETE | Deletes a contact from a Codemagic tester group. |
| [List Tester Group Contacts](actions/list-tester-group-contacts.md) | GET | Retrieves contacts for a specific Codemagic tester group. |

### Groups

| Action | Method | Description |
| --- | --- | --- |
| [Create App Tester Group](actions/create-app-tester-group.md) | POST | Creates a new tester group for a Codemagic app. |
| [Create App Variable Group](actions/create-app-variable-group.md) | POST | Creates a new variable group for a Codemagic app. |
| [Create Team Variable Group](actions/create-team-variable-group.md) | POST | Creates a new variable group for a Codemagic team. |
| [Get Tester Group](actions/get-tester-group.md) | GET | Retrieves a specific tester group from Codemagic. |
| [Get Variable Group](actions/get-variable-group.md) | GET | Retrieves a specific variable group from Codemagic. |
| [List App Tester Groups](actions/list-app-tester-groups.md) | GET | Retrieves tester groups for a specific Codemagic app. |
| [List App Variable Groups](actions/list-app-variable-groups.md) | GET | Retrieves variable groups for a specific Codemagic app. |
| [List Team Variable Groups](actions/list-team-variable-groups.md) | GET | Retrieves variable groups for a specific Codemagic team. |
| [Update Tester Group](actions/update-tester-group.md) | PUT | Updates an existing tester group in Codemagic. |
| [Update Variable Group](actions/update-variable-group.md) | PUT | Updates an existing variable group in Codemagic. |

### Memberships

| Action | Method | Description |
| --- | --- | --- |
| [List Team Members](actions/list-team-members.md) | GET | Retrieves members for a specific Codemagic team. |

### Notifications

| Action | Method | Description |
| --- | --- | --- |
| [List User Notifications](actions/list-user-notifications.md) | GET | Retrieves notifications for the authenticated Codemagic user. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [List OTA Projects](actions/list-ota-projects.md) | GET | Retrieves over-the-air update projects for a Codemagic team. |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Get OTA Team Usage](actions/get-ota-team-usage.md) | GET | Retrieves over-the-air update usage for a Codemagic team. |

### Secrets

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Import Variables For Group](actions/bulk-import-variables-for-group.md) | POST | Bulk imports variables into a Codemagic variable group. |
| [Get Variable](actions/get-variable.md) | GET | Retrieves a specific variable from a Codemagic group. |
| [List Variables For Group](actions/list-variables-for-group.md) | GET | Retrieves variables for a specific Codemagic variable group. |
| [Update Variable](actions/update-variable.md) | PUT | Updates an existing variable in a Codemagic group. |

### Teams

| Action | Method | Description |
| --- | --- | --- |
| [Get Team](actions/get-team.md) | GET | Retrieves a specific team from Codemagic. |
| [List Authenticated User Teams](actions/list-authenticated-user-teams.md) | GET | Retrieves teams for the authenticated Codemagic user. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Get Meta Information](actions/get-meta-information.md) | GET | Retrieves Codemagic meta information and public IP addresses. |
| [Get OTA Account Info](actions/get-ota-account-info.md) | GET | Retrieves over-the-air update account information from Codemagic. |
| [Get Shorebird Metadata](actions/get-shorebird-metadata.md) | GET | Retrieves Shorebird integration information from Codemagic. |

### User Profiles

| Action | Method | Description |
| --- | --- | --- |
| [Get User Preferences](actions/get-user-preferences.md) | GET | Retrieves preferences for the authenticated Codemagic user. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Authenticated User](actions/get-authenticated-user.md) | GET | Retrieves the authenticated user from Codemagic. |

