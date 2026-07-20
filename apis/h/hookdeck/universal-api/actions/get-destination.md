# Hookdeck: Get Destination

Retrieves a destination from Hookdeck.

```
GET https://connect.mindcloud.co/v1/universal/hookdeck/latest/actions/get-destination
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hookdeck `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hookdeck/latest/actions/get-destination?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hookdeck/latest/actions/get-destination?${params}`, {
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
| `id` | string | yes | Hookdeck destination ID from the `id` path parameter. |

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

Through the native Hookdeck API, this operation is `GET /destinations/:id` (base URL `https://api.hookdeck.com/2025-07-01`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-destination.md) for the provider-specific parameters and requirements.

