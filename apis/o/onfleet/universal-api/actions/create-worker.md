# Onfleet: Create Worker

Creates a new worker in Onfleet.

```
POST https://connect.mindcloud.co/v1/universal/onfleet/latest/actions/create-worker
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Onfleet `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/onfleet/latest/actions/create-worker" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "phone": "string",
  "teams[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/onfleet/latest/actions/create-worker', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "phone": "string",
    "teams[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | The worker's complete name. |
| `phone` | string | yes | The worker's phone number. |
| `teams[]` | array<string> | yes | One or more team IDs of which the worker is a member. |
| `capacity` | number | no | The maximum number of units this worker can carry. |
| `displayName` | string | no | The display name used in SMS notifications and tracking pages. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountStatus": "string",
      "capacity": 1,
      "displayName": "Ava Chen",
      "id": "string",
      "name": "Ava Chen",
      "onDuty": true,
      "phone": "string",
      "teams": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountStatus` | string |  |
| `capacity` | number |  |
| `displayName` | string |  |
| `id` | string |  |
| `name` | string |  |
| `onDuty` | boolean |  |
| `phone` | string |  |
| `teams` | array<string> |  |

## Native endpoint

Through the native Onfleet API, this operation is `POST /workers` (base URL `https://onfleet.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-worker.md) for the provider-specific parameters and requirements.

