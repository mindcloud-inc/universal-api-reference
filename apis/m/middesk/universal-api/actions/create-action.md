# Middesk: Create an action on an object

Creates an action on an object in Middesk.

```
POST https://connect.mindcloud.co/v1/universal/middesk/latest/actions/create-action
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Middesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/middesk/latest/actions/create-action" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "objectId": "string",
  "objectType": "string",
  "payload": {},
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/middesk/latest/actions/create-action', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "objectId": "string",
    "objectType": "string",
    "payload": {},
    "type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `objectId` | string | yes | ID of the object to create the action on. |
| `objectType` | string | yes | Type of object to create the action on. |
| `payload` | object | yes | Payload for the requested action. |
| `type` | string | yes | Action type to create. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actors": [
        {}
      ],
      "createdAt": "string",
      "effects": [
        {}
      ],
      "id": "string",
      "metadata": {},
      "note": "string",
      "objectId": "string",
      "objectType": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actors` | array<object> |  |
| `createdAt` | string |  |
| `effects` | array<object> |  |
| `id` | string |  |
| `metadata` | object |  |
| `note` | string |  |
| `objectId` | string |  |
| `objectType` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Middesk API, this operation is `POST /actions` (base URL `https://api.middesk.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-action.md) for the provider-specific parameters and requirements.

