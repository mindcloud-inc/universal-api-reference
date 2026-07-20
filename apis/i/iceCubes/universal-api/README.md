# <img src="https://images.mindcloud.co/apps/icons/ice-cubes_1774871340639.png" alt="IceCubes logo" width="28" height="28"> IceCubes: Universal API

Access meetings, transcripts, action items, contacts, and insights

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/iceCubes/latest
- **Category:** Communication / Video Communications
- **Actions:** 13
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://icecubes.app
- **Vendor API docs:** https://icecubes.app/docs/api/rest

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get User](actions/get-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iceCubes/latest/actions/get-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (13)

### Action Item

| Action | Method | Description |
| --- | --- | --- |
| [Create Action Item](actions/create-action-item.md) | POST |  |
| [List Action Items](actions/list-action-items.md) | GET |  |
| [Update Action Item](actions/update-action-item.md) | PUT |  |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [List Contacts](actions/list-contacts.md) | GET |  |

### Meeting

| Action | Method | Description |
| --- | --- | --- |
| [Get Meeting](actions/get-meeting.md) | GET |  |
| [Get Meeting Insights](actions/get-meeting-insights.md) | GET |  |
| [Get Meeting Notes](actions/get-meeting-notes.md) | GET |  |
| [Get Meeting Transcript](actions/get-meeting-transcript.md) | GET |  |
| [List Meetings](actions/list-meetings.md) | GET |  |
| [Search Meeting Content](actions/search-meeting-content.md) | GET |  |
| [Update Meeting Notes](actions/update-meeting-notes.md) | PUT |  |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [List Tags](actions/list-tags.md) | GET |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User](actions/get-user.md) | GET |  |

