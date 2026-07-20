# Wisewand: Get personas

Retrieves a persona from your Wisewand workspace.

```
GET https://connect.mindcloud.co/v1/universal/wisewand/latest/actions/get-personas
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wisewand `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wisewand/latest/actions/get-personas?connectionId=$CONNECTION_ID&id=test-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "test-id"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wisewand/latest/actions/get-personas?${params}`, {
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
| `id` | string | yes | Wisewand path parameter `id`. Default: `test-id`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "id": "string",
      "last_example": "string",
      "name": "Ava Chen",
      "picture": "string",
      "resume": "string",
      "style": "string",
      "type": "string",
      "user_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string |  |
| `id` | string |  |
| `last_example` | string |  |
| `name` | string |  |
| `picture` | string |  |
| `resume` | string |  |
| `style` | string |  |
| `type` | string |  |
| `user_id` | string |  |

## Native endpoint

Through the native Wisewand API, this operation is `GET /v1/personas/:id` (base URL `https://api.wisewand.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-personas.md) for the provider-specific parameters and requirements.

