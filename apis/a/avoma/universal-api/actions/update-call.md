# Avoma: Update Call

Updates an existing call in Avoma.

```
PUT https://connect.mindcloud.co/v1/universal/avoma/latest/actions/update-call
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Avoma `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/avoma/latest/actions/update-call" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "externalId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/avoma/latest/actions/update-call', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "externalId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `externalId` | string | yes | External ID of the call to update. |
| `subject` | string | no | Updated subject of the meeting associated with the call. |
| `meetingPurposeUuid` | string | no | Updated meeting type UUID associated with the call. |
| `meetingOutcomeUuid` | string | no | Updated meeting outcome UUID associated with the call. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "additionalDetails": "string",
      "answered": true,
      "direction": "string",
      "endAt": "2026-05-07T12:00:00.000Z",
      "externalId": "string",
      "frm": "string",
      "isVoicemail": true,
      "meeting": {
        "endAt": "2026-05-07T12:00:00.000Z",
        "organizerEmail": "ava@example.com",
        "startAt": "2026-05-07T12:00:00.000Z",
        "state": "string",
        "subject": "string",
        "uuid": "string"
      },
      "meetingOutcomeUuid": "string",
      "meetingPurposeUuid": "string",
      "organization": {
        "domain": "string",
        "name": "Ava Chen"
      },
      "recordingUrl": "https://example.com",
      "source": "string",
      "startAt": "2026-05-07T12:00:00.000Z",
      "state": "string",
      "subject": "string",
      "to": "string",
      "userEmail": "ava@example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `additionalDetails` | string |  |
| `answered` | boolean |  |
| `direction` | string |  |
| `endAt` | date |  |
| `externalId` | string |  |
| `frm` | string |  |
| `isVoicemail` | boolean |  |
| `meeting.endAt` | date |  |
| `meeting.organizerEmail` | string |  |
| `meeting.startAt` | date |  |
| `meeting.state` | string |  |
| `meeting.subject` | string |  |
| `meeting.uuid` | string |  |
| `meetingOutcomeUuid` | string |  |
| `meetingPurposeUuid` | string |  |
| `organization.domain` | string |  |
| `organization.name` | string |  |
| `recordingUrl` | string |  |
| `source` | string |  |
| `startAt` | date |  |
| `state` | string |  |
| `subject` | string |  |
| `to` | string |  |
| `userEmail` | string |  |

## Native endpoint

Through the native Avoma API, this operation is `PATCH /v1/calls/:external_id/` (base URL `https://api.avoma.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-call.md) for the provider-specific parameters and requirements.

