# <img src="https://images.mindcloud.co/apps/icons/grain_1772219699662.png" alt="Grain logo" width="28" height="28"> Grain: Universal API

Record meetings, share highlights, summarize calls, and coach teams.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/grain/latest
- **Category:** Communication / Video Communications
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://grain.com
- **Vendor API docs:** https://developers.grain.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Teams](actions/list-teams.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/grain/latest/actions/list-teams?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Hook

| Action | Method | Description |
| --- | --- | --- |
| [Create Hook](actions/create-hook.md) | POST | Creates a new hook in Grain. |
| [Delete Hook](actions/delete-hook.md) | DELETE | Deletes a hook from Grain. |
| [List Hooks](actions/list-hooks.md) | GET | Retrieves hooks from Grain. |

### Meeting Type

| Action | Method | Description |
| --- | --- | --- |
| [List Meeting Types](actions/list-meeting-types.md) | GET | Retrieves meeting types from Grain. |

### Recording

| Action | Method | Description |
| --- | --- | --- |
| [Add Tag to Recording](actions/add-tag-to-recording.md) | PUT | Adds a tag to a recording in Grain. |
| [Download Recording](actions/download-recording.md) | GET | Downloads a recording from Grain. |
| [Get Recording](actions/get-recording.md) | GET | Retrieves a recording from Grain. |
| [Get Recording Transcript JSON](actions/get-recording-transcript-json.md) | GET | Retrieves a recording transcript in JSON from Grain. |
| [Get Recording Transcript SRT](actions/get-recording-transcript-srt.md) | GET | Retrieves a recording transcript in SRT from Grain. |
| [Get Recording Transcript TXT](actions/get-recording-transcript-txt.md) | GET | Retrieves a recording transcript in TXT from Grain. |
| [Get Recording Transcript VTT](actions/get-recording-transcript-vtt.md) | GET | Retrieves a recording transcript in VTT from Grain. |
| [List Recordings](actions/list-recordings.md) | GET | Retrieves recordings from Grain. |
| [Remove Tag from Recording](actions/remove-tag-from-recording.md) | DELETE | Removes a tag from a recording in Grain. |
| [Share Recording to Team](actions/share-recording-to-team.md) | PUT | Shares a recording with a team in Grain. |
| [Share Recording to User](actions/share-recording-to-user.md) | PUT | Shares a recording with a user in Grain. |
| [Unshare Recording from Team](actions/unshare-recording-from-team.md) | DELETE | Unshares a recording from a team in Grain. |
| [Unshare Recording from User](actions/unshare-recording-from-user.md) | DELETE | Unshares a recording from a user in Grain. |
| [Update Recording](actions/update-recording.md) | PUT | Updates an existing recording in Grain. |

### Team

| Action | Method | Description |
| --- | --- | --- |
| [List Teams](actions/list-teams.md) | GET | Retrieves workspace teams from Grain. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [List Users](actions/list-users.md) | GET | Retrieves workspace users from Grain. |

