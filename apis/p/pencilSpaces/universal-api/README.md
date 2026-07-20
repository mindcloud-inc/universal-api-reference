# <img src="https://images.mindcloud.co/apps/icons/favicon-2_1774976491989.png" alt="Pencil Spaces logo" width="28" height="28"> Pencil Spaces: Universal API

Manage learning spaces, events, attendance, recordings, and transcripts

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/pencilSpaces/latest
- **Category:** Human Resources / Learning (LMS)
- **Actions:** 18
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://pencilspaces.com/
- **Vendor API docs:** https://api.pencilspaces.com/guide

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Custom Attributes](actions/list-custom-attributes.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pencilSpaces/latest/actions/list-custom-attributes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (18)

### Attributes

| Action | Method | Description |
| --- | --- | --- |
| [List Custom Attributes](actions/list-custom-attributes.md) | GET |  |

### Audit Entries

| Action | Method | Description |
| --- | --- | --- |
| [Get Audit History](actions/get-audit-history.md) | GET |  |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [Create Event](actions/create-event.md) | POST |  |
| [Delete Event](actions/delete-event.md) | DELETE |  |
| [Get Event](actions/get-event.md) | GET |  |
| [Update Event](actions/update-event.md) | PUT |  |

### Recordings

| Action | Method | Description |
| --- | --- | --- |
| [List Space Recordings](actions/list-space-recordings.md) | GET |  |

### Session

| Action | Method | Description |
| --- | --- | --- |
| [Delete Session](actions/delete-session.md) | DELETE |  |
| [End Ongoing Session](actions/end-ongoing-session.md) | PUT |  |
| [Get Session](actions/get-session.md) | GET |  |

### Sessions

| Action | Method | Description |
| --- | --- | --- |
| [List Sessions](actions/list-sessions.md) | GET |  |

### Space

| Action | Method | Description |
| --- | --- | --- |
| [Create Space](actions/create-space.md) | POST |  |
| [Delete Space](actions/delete-space.md) | DELETE |  |
| [Get Space](actions/get-space.md) | GET |  |
| [Update Space](actions/update-space.md) | PUT |  |
| [Update Space User Roles](actions/update-space-user-roles.md) | PUT |  |

### Space Settings

| Action | Method | Description |
| --- | --- | --- |
| [Update Space Settings](actions/update-space-settings.md) | PUT |  |

### Spaces

| Action | Method | Description |
| --- | --- | --- |
| [List Spaces](actions/list-spaces.md) | GET |  |

