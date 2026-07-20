# Hookdeck: Get Connection

Retrieves a connection from Hookdeck.

```
GET https://connect.mindcloud.co/v1/universal/hookdeck/latest/actions/get-connection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hookdeck `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hookdeck/latest/actions/get-connection?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hookdeck/latest/actions/get-connection?${params}`, {
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

Through the native Hookdeck API, this operation is `GET /connections/:id` (base URL `https://api.hookdeck.com/2025-07-01`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-connection.md) for the provider-specific parameters and requirements.

