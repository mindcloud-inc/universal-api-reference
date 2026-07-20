# <img src="https://images.mindcloud.co/apps/icons/stormboard_1775671722576.png" alt="Stormboard logo" width="28" height="28"> Stormboard: Universal API

Stormboard is a data-first collaborative workflow platform and digital whiteboard for turning collaboration into structured, actionable work.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/stormboard/latest
- **Category:** Productivity / Project Management
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://stormboard.com
- **Vendor API docs:** https://api.stormboard.com/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Check Authentication](actions/check-authentication.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stormboard/latest/actions/check-authentication?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Access

| Action | Method | Description |
| --- | --- | --- |
| [Get Storm Access](actions/get-storm-access.md) | GET | Retrieves your access level for a Storm in Stormboard. |

### Comment

| Action | Method | Description |
| --- | --- | --- |
| [Create Comment](actions/create-comment.md) | POST | Creates a comment on an idea in Stormboard. |
| [List Comments](actions/list-comments.md) | GET | Retrieves comments for an idea in Stormboard. |

### Idea

| Action | Method | Description |
| --- | --- | --- |
| [Create Idea](actions/create-idea.md) | POST | Creates an idea in Stormboard. |
| [Delete Idea](actions/delete-idea.md) | DELETE | Deletes an idea from Stormboard. |
| [Get Idea Data](actions/get-idea-data.md) | GET | Retrieves idea data from Stormboard. |
| [List Storm Ideas](actions/list-storm-ideas.md) | GET | Retrieves ideas from a Storm in Stormboard. |
| [Update Idea](actions/update-idea.md) | PUT | Updates an idea in Stormboard. |

### Invitation

| Action | Method | Description |
| --- | --- | --- |
| [Accept Storm Invite](actions/accept-storm-invite.md) | POST | Accepts a Storm invite in Stormboard. |
| [Decline Storm Invite](actions/decline-storm-invite.md) | POST | Declines a Storm invite in Stormboard. |
| [Invite Participants](actions/invite-participants.md) | POST | Invites participants to a Storm in Stormboard. |
| [List Storm Invites](actions/list-storm-invites.md) | GET | Retrieves your Storm invites from Stormboard. |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Create Chat Message](actions/create-chat-message.md) | POST | Creates a chat message in Stormboard. |
| [List Chat Messages](actions/list-chat-messages.md) | GET | Retrieves chat messages from a Storm in Stormboard. |

### Participant

| Action | Method | Description |
| --- | --- | --- |
| [List Storm Participants](actions/list-storm-participants.md) | GET | Retrieves participants from a Storm in Stormboard. |

### Storm

| Action | Method | Description |
| --- | --- | --- |
| [Create Storm](actions/create-storm.md) | POST | Creates a Storm in Stormboard. |
| [Get Storm Details](actions/get-storm-details.md) | GET | Retrieves Storm details from Stormboard. |
| [Join Storm](actions/join-storm.md) | POST | Joins a Storm in Stormboard. |
| [Leave Storm](actions/leave-storm.md) | POST | Leaves a Storm in Stormboard. |
| [List Storms](actions/list-storms.md) | GET | Retrieves your Storms from Stormboard. |
| [Update Storm](actions/update-storm.md) | PUT | Updates a Storm in Stormboard. |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Update Idea Task](actions/update-idea-task.md) | PUT | Updates an idea task in Stormboard. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Check Authentication](actions/check-authentication.md) | GET | Checks whether your Stormboard authentication token is valid. |
| [Get User Profile](actions/get-user-profile.md) | GET | Retrieves your Stormboard user profile. |

