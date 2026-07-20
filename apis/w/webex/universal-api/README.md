# <img src="https://images.mindcloud.co/apps/icons/webex_1777583632020.png" alt="Webex logo" width="28" height="28"> Webex: Universal API

Use Cisco Webex APIs for messaging spaces, messages, memberships, teams, meetings, webhooks, and user profile details.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/webex/latest
- **Actions:** 31
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.webex.com/
- **Vendor API docs:** https://developer.webex.com/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get My Own Details](actions/get-my-own-details.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webex/latest/actions/get-my-own-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (31)

### Meeting

| Action | Method | Description |
| --- | --- | --- |
| [Create Meeting](actions/create-meeting.md) | POST | Creates a new meeting in Webex. |
| [Delete Meeting](actions/delete-meeting.md) | DELETE | Deletes an existing meeting from Webex. |
| [Get Meeting](actions/get-meeting.md) | GET | Retrieves a specific meeting from Webex. |
| [List Meetings](actions/list-meetings.md) | GET | Lists meetings in your Webex account. |
| [Update Meeting](actions/update-meeting.md) | PUT | Updates an existing meeting in Webex. |

### Membership

| Action | Method | Description |
| --- | --- | --- |
| [Create Membership](actions/create-membership.md) | POST | Creates a new membership in Webex. |
| [Delete Membership](actions/delete-membership.md) | DELETE | Deletes an existing membership from Webex. |
| [Get Membership](actions/get-membership.md) | GET | Retrieves a specific membership from Webex. |
| [List Memberships](actions/list-memberships.md) | GET | Lists memberships in your Webex account. |
| [Update Membership](actions/update-membership.md) | PUT | Updates an existing membership in Webex. |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Create Message](actions/create-message.md) | POST | Creates a new message in Webex. |
| [Delete Message](actions/delete-message.md) | DELETE | Deletes an existing message from Webex. |
| [Get Message](actions/get-message.md) | GET | Retrieves a specific message from Webex. |
| [List Messages](actions/list-messages.md) | GET | Lists messages in your Webex account. |
| [Update Message](actions/update-message.md) | PUT | Updates an existing message in Webex. |

### Person

| Action | Method | Description |
| --- | --- | --- |
| [Get My Own Details](actions/get-my-own-details.md) | GET | Retrieves your own profile details from Webex. |

### Room

| Action | Method | Description |
| --- | --- | --- |
| [Create Room](actions/create-room.md) | POST | Creates a new room in Webex. |
| [Delete Room](actions/delete-room.md) | DELETE | Deletes an existing room from Webex. |
| [Get Room](actions/get-room.md) | GET | Retrieves a specific room from Webex. |
| [List Rooms](actions/list-rooms.md) | GET | Lists messaging rooms in your Webex account. |
| [Update Room](actions/update-room.md) | PUT | Updates an existing room in Webex. |

### Team

| Action | Method | Description |
| --- | --- | --- |
| [Create Team](actions/create-team.md) | POST | Creates a new team in Webex. |
| [Delete Team](actions/delete-team.md) | DELETE | Deletes an existing team from Webex. |
| [Get Team](actions/get-team.md) | GET | Retrieves a specific team from Webex. |
| [List Teams](actions/list-teams.md) | GET | Lists teams in your Webex account. |
| [Update Team](actions/update-team.md) | PUT | Updates an existing team in Webex. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in Webex. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes an existing webhook from Webex. |
| [Get Webhook](actions/get-webhook.md) | GET | Retrieves a specific webhook from Webex. |
| [List Webhooks](actions/list-webhooks.md) | GET | Lists webhooks in your Webex account. |
| [Update Webhook](actions/update-webhook.md) | PUT | Updates an existing webhook in Webex. |

