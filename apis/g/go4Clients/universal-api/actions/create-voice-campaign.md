# Go4Clients: Create Voice Campaign

Creates a new voice campaign in Go4Clients.

```
POST https://connect.mindcloud.co/v1/universal/go4Clients/latest/actions/create-voice-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Go4Clients `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/go4Clients/latest/actions/create-voice-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "MindCloud voice campaign",
  "sender": "573112233445"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/go4Clients/latest/actions/create-voice-campaign', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "MindCloud voice campaign",
    "sender": "573112233445"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Campaign name to identify the call in analytics. Example: `MindCloud voice campaign`. |
| `sender` | string | yes | Caller ID shown to recipients. Example: `573112233445`. |
| `description` | string | no | Optional voice campaign description. Example: `MindCloud voice test`. |
| `callAttempts` | string | no | Number of call attempts per destination. Example: `2`. |
| `timeBetweenDials` | number | no | Minutes between call attempts. Example: `15`. |
| `currentCalls` | number | no | Maximum simultaneous calls. Example: `100`. |
| `earliestTimeToCall` | string | no | Earliest allowed local time in HH:mm format. Example: `06:00`. |
| `latestTimeToCall` | string | no | Latest allowed local time in HH:mm format. Example: `20:00`. |
| `nextDayContinuation` | boolean | no | Continue the campaign on the next day when the call window ends. Example: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "billingProduct": "string",
      "callAttempts": 1,
      "campaignType": "string",
      "creationDate": "2026-05-07T12:00:00.000Z",
      "currentCalls": 1,
      "earliestTimeToCall": "string",
      "id": "string",
      "latestTimeToCall": "string",
      "name": "Ava Chen",
      "nextDayContinuation": true,
      "sender": "string",
      "sendNow": true,
      "startDate": "2026-05-07T12:00:00.000Z",
      "timeBetweenDials": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billingProduct` | string | Billing product associated with the campaign. |
| `callAttempts` | number | Configured number of call attempts. |
| `campaignType` | string | Campaign type. |
| `creationDate` | date | Campaign creation date. |
| `currentCalls` | number | Maximum concurrent calls. |
| `earliestTimeToCall` | string | Earliest time to call. |
| `id` | string | Identifier of the voice campaign. |
| `latestTimeToCall` | string | Latest time to call. |
| `name` | string | Name of the voice campaign. |
| `nextDayContinuation` | boolean | Whether calls continue the next day. |
| `sender` | string | Sender associated with the voice campaign. |
| `sendNow` | boolean | Whether the campaign sends immediately. |
| `startDate` | date | Campaign start date. |
| `timeBetweenDials` | number | Time between dials in seconds. |

## Native endpoint

Through the native Go4Clients API, this operation is `POST /api/campaigns/voice/v1.0` (base URL `https://cloud.go4clients.com:8580`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-voice-campaign.md) for the provider-specific parameters and requirements.

