# Routee: Perform a voice conversation

Creates a voice conversation in Routee.

```
POST https://connect.mindcloud.co/v1/universal/routee/latest/actions/perform-a-voice-conversation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/routee/latest/actions/perform-a-voice-conversation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "to": {},
  "from": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/routee/latest/actions/perform-a-voice-conversation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "to": {},
    "from": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `to` | object | yes | The recipient of the call. The destination phone number. Format with a '+' and country code e.g., +3069485xxxxx (E.164 format). NOTE: limit 1 reqest per second |
| `from` | string | yes | The sender id for the call. NOTICE: Alphanumeric sender is not supported by all networks (e.g. Greek networks). Check restrictions and features here: https://go.routee.net/#/management/restrictions-and-features. |
| `dialPlan` | object | no | A combination of action verbs to be executed. Can not be empty. Use either "dialPlanUrl" or "dialPlan". |
| `dialPlanUrl` | string | no | The url which contains a combination of action verbs to be executed. Use either "dialPlanUrl" or "dialPlan". |
| `callback` | object | no | Defines the notification callback information for the progress of Voice conversation |
| `hangupDelay` | number | no | The time to wait for the call to be answered. Min value: 1. Max value: 60. |
| `maxDuration` | number | no | Defines the maximum duration. Min value: 1 |
| `machineDetection` | object | no | It is used to detect if the call is answered by human or machine and define the desired actions (in case of machine). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "dialPlans": [
        [
          {}
        ]
      ],
      "direction": "string",
      "from": "string",
      "machineDetection": {
        "strategy": "string"
      },
      "to": {
        "phone": "string"
      },
      "trackingId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `dialPlans[]` | array<object> |  |
| `dialPlans[].verbs[]` | array<object> |  |
| `dialPlans[].verbs[].bargeIn` | boolean |  |
| `dialPlans[].verbs[].fileURL` | string |  |
| `dialPlans[].verbs[].repeat` | number |  |
| `dialPlans[].verbs[].type` | string |  |
| `direction` | string |  |
| `from` | string |  |
| `machineDetection` | object |  |
| `machineDetection.strategy` | string |  |
| `to` | object |  |
| `to.phone` | string |  |
| `trackingId` | string |  |

## Native endpoint

Through the native Routee API, this operation is `POST /voice/conversation` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/perform-a-voice-conversation.md) for the provider-specific parameters and requirements.

