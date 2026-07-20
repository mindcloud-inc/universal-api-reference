# CallRail: Update Call

Updates a call in CallRail.

```
PUT https://connect.mindcloud.co/v1/universal/callRail/latest/actions/update-call
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CallRail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/callRail/latest/actions/update-call" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "account_id": "string",
  "call_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/callRail/latest/actions/update-call', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "account_id": "string",
    "call_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `account_id` | string | yes |  |
| `call_id` | string | yes |  |
| `tags[]` | array<string> | no |  |
| `append_tags` | boolean | no |  |
| `lead_status` | string | no |  |
| `value` | string | no |  |
| `note` | string | no |  |
| `customer_name` | string | no |  |
| `spam` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "answered": true,
      "businessPhoneNumber": "string",
      "customerCity": "string",
      "customerCountry": "string",
      "customerName": "Ava Chen",
      "customerPhoneNumber": "string",
      "customerState": "string",
      "direction": "string",
      "duration": 1,
      "id": "string",
      "leadExplanation": "string",
      "leadScore": "string",
      "recording": "string",
      "recordingDuration": 1,
      "recordingPlayer": "string",
      "startTime": "string",
      "trackingPhoneNumber": "string",
      "voicemail": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `answered` | boolean |  |
| `businessPhoneNumber` | string |  |
| `customerCity` | string |  |
| `customerCountry` | string |  |
| `customerName` | string |  |
| `customerPhoneNumber` | string |  |
| `customerState` | string |  |
| `direction` | string |  |
| `duration` | number |  |
| `id` | string |  |
| `leadExplanation` | string |  |
| `leadScore` | string |  |
| `recording` | string |  |
| `recordingDuration` | number |  |
| `recordingPlayer` | string |  |
| `startTime` | string |  |
| `trackingPhoneNumber` | string |  |
| `voicemail` | boolean |  |

## Native endpoint

Through the native CallRail API, this operation is `PUT /v3/a/:account_id/calls/:call_id.json` (base URL `https://api.callrail.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-call.md) for the provider-specific parameters and requirements.

