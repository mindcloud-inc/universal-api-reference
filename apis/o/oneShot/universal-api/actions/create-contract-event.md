# 1Shot: Create Contract Event

Creates a new contract event in 1Shot API.

```
POST https://connect.mindcloud.co/v1/universal/oneShot/latest/actions/create-contract-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 1Shot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/oneShot/latest/actions/create-contract-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "businessId": "string",
  "chainId": 1,
  "contractAddress": "string",
  "name": "Ava Chen",
  "description": "string",
  "eventName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/oneShot/latest/actions/create-contract-event', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "businessId": "string",
    "chainId": 1,
    "contractAddress": "string",
    "name": "Ava Chen",
    "description": "string",
    "eventName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `businessId` | string | yes |  |
| `chainId` | number | yes |  |
| `contractAddress` | string | yes |  |
| `name` | string | yes |  |
| `description` | string | yes |  |
| `eventName` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "businessId": "string",
      "chainId": 1,
      "contractAddress": "string",
      "created": 1,
      "description": "string",
      "eventName": "Ava Chen",
      "id": "string",
      "name": "Ava Chen",
      "topicHash": "string",
      "topics": [
        {
          "indexed": true,
          "name": "Ava Chen"
        }
      ],
      "updated": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `businessId` | string |  |
| `chainId` | number |  |
| `contractAddress` | string |  |
| `created` | number |  |
| `description` | string |  |
| `eventName` | string |  |
| `id` | string |  |
| `name` | string |  |
| `topicHash` | string |  |
| `topics[].indexed` | boolean |  |
| `topics[].name` | string |  |
| `updated` | number |  |

## Native endpoint

Through the native 1Shot API, this operation is `POST /business/:businessId/events` (base URL `https://api.1shotapi.com/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contract-event.md) for the provider-specific parameters and requirements.

