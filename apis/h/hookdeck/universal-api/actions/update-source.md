# Hookdeck: Update Source

Updates an existing source in Hookdeck.

```
PUT https://connect.mindcloud.co/v1/universal/hookdeck/latest/actions/update-source
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hookdeck `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/hookdeck/latest/actions/update-source" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "body": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hookdeck/latest/actions/update-source', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "body": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Hookdeck source ID from the `id` path parameter. |
| `body` | object | yes | JSON request body for updating a Hookdeck source. Use the documented source update schema. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authenticated": true,
      "config": {},
      "created_at": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "disabled_at": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen",
      "team_id": "string",
      "type": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authenticated` | boolean |  |
| `config` | object |  |
| `created_at` | date |  |
| `description` | string |  |
| `disabled_at` | date |  |
| `id` | string |  |
| `name` | string |  |
| `team_id` | string |  |
| `type` | string |  |
| `updated_at` | date |  |
| `url` | string |  |

## Native endpoint

Through the native Hookdeck API, this operation is `PUT /sources/:id` (base URL `https://api.hookdeck.com/2025-07-01`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-source.md) for the provider-specific parameters and requirements.

