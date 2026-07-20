# InsightIQ: Get User

Retrieves a single user from InsightIQ.

```
GET https://connect.mindcloud.co/v1/universal/insightIQ/latest/actions/get-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InsightIQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/insightIQ/latest/actions/get-user?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/insightIQ/latest/actions/get-user?${params}`, {
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
| `id` | string | yes | InsightIQ user identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "external_id": "string",
      "id": "string",
      "name": "Ava Chen",
      "status": "string",
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
| `external_id` | string |  |
| `id` | string |  |
| `name` | string |  |
| `status` | string |  |
| `updated_at` | date |  |

## Native endpoint

Through the native InsightIQ API, this operation is `GET /v1/users/:id` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user.md) for the provider-specific parameters and requirements.

