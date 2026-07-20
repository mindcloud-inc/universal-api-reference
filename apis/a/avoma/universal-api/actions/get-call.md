# Avoma: Get Call

Retrieves a call by external ID from Avoma.

```
GET https://connect.mindcloud.co/v1/universal/avoma/latest/actions/get-call
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Avoma `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/avoma/latest/actions/get-call?connectionId=$CONNECTION_ID&externalId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "externalId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/avoma/latest/actions/get-call?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `externalId` | string | yes | External ID of the call. |

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

Through the native Avoma API, this operation is `GET /v1/calls/:external_id/` (base URL `https://api.avoma.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-call.md) for the provider-specific parameters and requirements.

