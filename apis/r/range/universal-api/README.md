# <img src="https://images.mindcloud.co/apps/icons/range_1775059308548.png" alt="Range logo" width="28" height="28"> Range: Universal API

Range is a team check-in and update platform. Use this app to read users, teams, updates, and activity data in Range and to manage supported team and user actions through the official Range API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/range/latest
- **Category:** Communication / Team Messaging
- **Actions:** 14
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.range.co
- **Vendor API docs:** https://www.range.co/docs/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Auth User](actions/get-auth-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/range/latest/actions/get-auth-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (14)

### Activity

| Action | Method | Description |
| --- | --- | --- |
| [Record Activity](actions/record-activity.md) | POST | Record an activity interaction for a user with attachment data. |

### Team

| Action | Method | Description |
| --- | --- | --- |
| [Create Team](actions/create-team.md) | POST | Create a new team with optional parent and mascot. |
| [Get Team](actions/get-team.md) | GET | Retrieve a team by its Range team ID. |
| [List Teams](actions/list-teams.md) | GET | List workspace teams with optional archived and following filters. |
| [List User Teams](actions/list-user-teams.md) | GET | List a user's teams with optional archived and following filters. |

### Team Relation

| Action | Method | Description |
| --- | --- | --- |
| [Delete Team Relation](actions/delete-team-relation.md) | DELETE | Remove the relationship between a team and user. |
| [Update Team Relation](actions/update-team-relation.md) | PUT | Update the relationship between a team and user. |

### Update

| Action | Method | Description |
| --- | --- | --- |
| [List Updates](actions/list-updates.md) | GET | List updates with optional target, teammate, and time filters. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Find User](actions/find-user.md) | GET | Find a user by email or identity provider details. |
| [Get Auth User](actions/get-auth-user.md) | GET | Retrieve the authenticated user and active organization session details. |
| [Get User](actions/get-user.md) | GET | Retrieve a user by its Range user ID. |
| [List Org Users](actions/list-org-users.md) | GET | List organization users with optional team and relation filters. |

### User Profile

| Action | Method | Description |
| --- | --- | --- |
| [Update User Profile](actions/update-user-profile.md) | PUT | Update a user's profile fields with partial profile data. |

### User State

| Action | Method | Description |
| --- | --- | --- |
| [Update User State](actions/update-user-state.md) | PUT | Update a user's state fields with partial state data. |

