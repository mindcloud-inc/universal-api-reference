# ECAL: Remove Subscriber Subscriptions

Removes calendar subscriptions from an ECAL subscriber.

```
PUT https://connect.mindcloud.co/v1/universal/eCAL/latest/actions/remove-subscriber-subscriptions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ECAL `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/eCAL/latest/actions/remove-subscriber-subscriptions" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "ecalId": "string",
  "requestBody": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eCAL/latest/actions/remove-subscriber-subscriptions', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "ecalId": "string",
    "requestBody": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ecalId` | string | yes | Subscriber ecal_id value. |
| `requestBody` | object | yes | JSON object matching ECAL's remove subscriptions body, including calendar identifiers as documented. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "calendarIds": [
        "string"
      ],
      "ecalId": "string",
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `calendarIds` | array<string> |  |
| `ecalId` | string |  |
| `message` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native ECAL API, this operation is `POST /subscriber/:ecalId/subscriptions/remove` (base URL `https://api.ecal.com/apiv2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-subscriber-subscriptions.md) for the provider-specific parameters and requirements.

