# <img src="https://images.mindcloud.co/apps/icons/swit_1774468463938.png" alt="Swit logo" width="28" height="28"> Swit: Universal API

Connect Swit workspaces to manage teams, users, and messaging through the official Swit APIs and app-install OAuth flow.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/swit/latest
- **Category:** Communication / Team Messaging
- **Actions:** 6
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://swit.io
- **Vendor API docs:** https://tech-support.swit.io/books/swit-java-development-guide

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Teams](actions/list-teams.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/swit/latest/actions/list-teams?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (6)

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Create Message](actions/create-message.md) | POST | Creates a new message in Swit. |

### Team

| Action | Method | Description |
| --- | --- | --- |
| [Add Users To Team](actions/add-users-to-team.md) | PUT | Adds users to a team in Swit. |
| [Create Team](actions/create-team.md) | POST | Creates a new team in Swit. |
| [List Teams](actions/list-teams.md) | GET | Retrieves teams and member IDs from Swit. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Create User](actions/create-user.md) | POST | Creates a new user in Swit. |
| [List Users](actions/list-users.md) | GET | Retrieves users from Swit with paginated results. |

