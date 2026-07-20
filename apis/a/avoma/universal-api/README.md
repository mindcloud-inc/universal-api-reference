# <img src="https://images.mindcloud.co/apps/icons/avoma_1773843227254.png" alt="Avoma logo" width="28" height="28"> Avoma: Universal API

Manage Avoma meetings, notes, recordings, and conversation insights

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/avoma/latest
- **Category:** Communication / Video Communications
- **Actions:** 25
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.avoma.com
- **Vendor API docs:** https://dev.avoma.com

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Users](actions/list-users.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/avoma/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (25)

### Call

| Action | Method | Description |
| --- | --- | --- |
| [Create Call](actions/create-call.md) | POST | Creates a new call in Avoma. |
| [Get Call](actions/get-call.md) | GET | Retrieves a call by external ID from Avoma. |
| [List Calls](actions/list-calls.md) | GET | Retrieves calls from Avoma. |
| [Update Call](actions/update-call.md) | PUT | Updates an existing call in Avoma. |

### Meeting

| Action | Method | Description |
| --- | --- | --- |
| [Get Meeting](actions/get-meeting.md) | GET | Retrieves a meeting from Avoma. |
| [List Meetings](actions/list-meetings.md) | GET | Retrieves meetings from Avoma. |

### Meetinginsight

| Action | Method | Description |
| --- | --- | --- |
| [Get Meeting Insights](actions/get-meeting-insights.md) | GET | Retrieves insights for a completed meeting from Avoma. |

### Meetingoutcome

| Action | Method | Description |
| --- | --- | --- |
| [Create Meeting Outcome](actions/create-meeting-outcome.md) | POST | Creates a new meeting outcome in Avoma. |
| [Delete Meeting Outcome](actions/delete-meeting-outcome.md) | DELETE | Deletes an existing meeting outcome from Avoma. |
| [Get Meeting Outcome](actions/get-meeting-outcome.md) | GET | Retrieves a meeting outcome from Avoma. |
| [List Meeting Outcomes](actions/list-meeting-outcomes.md) | GET | Retrieves meeting outcomes from Avoma. |
| [Update Meeting Outcome](actions/update-meeting-outcome.md) | PUT | Updates an existing meeting outcome in Avoma. |

### Meetingsegment

| Action | Method | Description |
| --- | --- | --- |
| [Get Meeting Segments](actions/get-meeting-segments.md) | GET | Retrieves segments for a meeting from Avoma. |

### Meetingsentiment

| Action | Method | Description |
| --- | --- | --- |
| [Get Meeting Sentiments](actions/get-meeting-sentiments.md) | GET | Retrieves sentiments for a meeting from Avoma. |

### Meetingtype

| Action | Method | Description |
| --- | --- | --- |
| [Create Meeting Type](actions/create-meeting-type.md) | POST | Creates a new meeting type in Avoma. |
| [Delete Meeting Type](actions/delete-meeting-type.md) | DELETE | Deletes an existing meeting type from Avoma. |
| [Get Meeting Type](actions/get-meeting-type.md) | GET | Retrieves a meeting type from Avoma. |
| [List Meeting Types](actions/list-meeting-types.md) | GET | Retrieves meeting types from Avoma. |
| [Update Meeting Type](actions/update-meeting-type.md) | PUT | Updates an existing meeting type in Avoma. |

### Note

| Action | Method | Description |
| --- | --- | --- |
| [List Notes](actions/list-notes.md) | GET | Retrieves notes from Avoma. |

### Recording

| Action | Method | Description |
| --- | --- | --- |
| [Get Recording](actions/get-recording.md) | GET | Retrieves a recording for a meeting from Avoma. |
| [Get Recording By UUID](actions/get-recording-by-uuid.md) | GET | Retrieves a recording by UUID from Avoma. |

### Transcription

| Action | Method | Description |
| --- | --- | --- |
| [Get Transcription](actions/get-transcription.md) | GET | Retrieves a transcription from Avoma. |
| [List Transcriptions](actions/list-transcriptions.md) | GET | Retrieves transcriptions from Avoma. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [List Users](actions/list-users.md) | GET | Retrieves users from Avoma. |

