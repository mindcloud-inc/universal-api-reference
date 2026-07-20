# Hookdeck: Create Destination

Creates a new destination in Hookdeck.

```
POST https://connect.mindcloud.co/v1/universal/hookdeck/latest/actions/create-destination
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hookdeck `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hookdeck/latest/actions/create-destination" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "body": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hookdeck/latest/actions/create-destination', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "body": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `body` | object | yes | JSON request body for creating a Hookdeck destination. Use the documented destination create schema. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "config": {},
      "created_at": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "disabled_at": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen",
      "team_id": "string",
      "type": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `config` | object |  |
| `created_at` | date |  |
| `description` | string |  |
| `disabled_at` | date |  |
| `id` | string |  |
| `name` | string |  |
| `team_id` | string |  |
| `type` | string |  |
| `updated_at` | date |  |

## Native endpoint

Through the native Hookdeck API, this operation is `POST /destinations` (base URL `https://api.hookdeck.com/2025-07-01`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-destination.md) for the provider-specific parameters and requirements.

