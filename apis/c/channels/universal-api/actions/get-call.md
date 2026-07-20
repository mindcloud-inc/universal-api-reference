# Channels: Get Call

Retrieves a call from Channels.

```
GET https://connect.mindcloud.co/v1/universal/channels/latest/actions/get-call
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Channels `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/channels/latest/actions/get-call?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/channels/latest/actions/get-call?${params}`, {
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
| `id` | number | yes | Call ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agentMsisdn": "string",
      "agentMsisdnIsoCountry": "string",
      "agentMsisdnLabel": "string",
      "agentName": "Ava Chen",
      "agentSurname": "Ava Chen",
      "agentUsername": "Ava Chen",
      "answered": true,
      "answeredDate": "2026-05-07T12:00:00.000Z",
      "appType": "string",
      "contactName": "Ava Chen",
      "contactSurname": "Ava Chen",
      "direction": "string",
      "finishDate": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "lengthSeconds": 1,
      "msisdn": "string",
      "recordEventType": "string",
      "recordId": 1,
      "recordingExists": true,
      "startDate": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agentMsisdn` | string |  |
| `agentMsisdnIsoCountry` | string |  |
| `agentMsisdnLabel` | string |  |
| `agentName` | string |  |
| `agentSurname` | string |  |
| `agentUsername` | string |  |
| `answered` | boolean |  |
| `answeredDate` | date |  |
| `appType` | string |  |
| `contactName` | string |  |
| `contactSurname` | string |  |
| `direction` | string |  |
| `finishDate` | date |  |
| `id` | number |  |
| `lengthSeconds` | number |  |
| `msisdn` | string |  |
| `recordEventType` | string |  |
| `recordId` | number |  |
| `recordingExists` | boolean |  |
| `startDate` | date |  |

## Native endpoint

Through the native Channels API, this operation is `GET /api/v1/calls/{id}` (base URL `https://api.channels.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-call.md) for the provider-specific parameters and requirements.

