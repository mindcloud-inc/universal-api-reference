# Avoma: Create Call

Creates a new call in Avoma.

```
POST https://connect.mindcloud.co/v1/universal/avoma/latest/actions/create-call
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Avoma `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/avoma/latest/actions/create-call" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "externalId": "string",
  "userEmail": "ava@example.com",
  "fromNumber": "string",
  "toNumber": "string",
  "startAt": "string",
  "recordingUrl": "https://example.com",
  "direction": "string",
  "source": "string",
  "participants[].email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/avoma/latest/actions/create-call', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "externalId": "string",
    "userEmail": "ava@example.com",
    "fromNumber": "string",
    "toNumber": "string",
    "startAt": "string",
    "recordingUrl": "https://example.com",
    "direction": "string",
    "source": "string",
    "participants[].email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `externalId` | string | yes | Unique ID of the call from the dialer system. |
| `userEmail` | string | yes | Email of the Avoma user who made or received the call. |
| `fromNumber` | string | yes | Phone number from which the call was made. |
| `toNumber` | string | yes | Phone number to which the call was made. |
| `startAt` | string | yes | Start time of the call in ISO 8601 UTC format. |
| `recordingUrl` | string | yes | Public URL of the call recording for Avoma to download and process. |
| `direction` | string | yes | Direction of the call, for example inbound or outbound. |
| `source` | string | yes | Lowercase source of the call, for example ringcentral or twilio. |
| `participants[].email` | string | yes | Email address of a participant. The first participant should be the prospect or lead. |
| `participants[].name` | string | no | Name of a participant. |
| `subject` | string | no | Subject of the meeting associated with the call. |
| `meetingPurposeUuid` | string | no | UUID of the meeting type associated with the call. |
| `meetingOutcomeUuid` | string | no | UUID of the meeting outcome associated with the call. |

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

Through the native Avoma API, this operation is `POST /v1/calls/` (base URL `https://api.avoma.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-call.md) for the provider-specific parameters and requirements.

