# Hookdeck: Unpause Connection

Unpauses a connection in Hookdeck.

```
PUT https://connect.mindcloud.co/v1/universal/hookdeck/latest/actions/unpause-connection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hookdeck `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/hookdeck/latest/actions/unpause-connection" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hookdeck/latest/actions/unpause-connection', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Hookdeck connection ID from the `id` path parameter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "destination": {},
      "disabled_at": "2026-05-07T12:00:00.000Z",
      "full_name": "Ava Chen",
      "id": "string",
      "name": "Ava Chen",
      "paused_at": "2026-05-07T12:00:00.000Z",
      "rules": [
        {}
      ],
      "source": {},
      "team_id": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date |  |
| `description` | string |  |
| `destination` | object |  |
| `disabled_at` | date |  |
| `full_name` | string |  |
| `id` | string |  |
| `name` | string |  |
| `paused_at` | date |  |
| `rules` | array<object> |  |
| `source` | object |  |
| `team_id` | string |  |
| `updated_at` | date |  |

## Native endpoint

Through the native Hookdeck API, this operation is `PUT /connections/:id/unpause` (base URL `https://api.hookdeck.com/2025-07-01`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/unpause-connection.md) for the provider-specific parameters and requirements.

