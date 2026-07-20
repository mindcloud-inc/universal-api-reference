# Uwear.ai: Get Avatar Details

Retrieves avatar details from Uwear.ai.

```
GET https://connect.mindcloud.co/v1/universal/uwearai/latest/actions/get-avatar-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Uwear.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uwearai/latest/actions/get-avatar-details?connectionId=$CONNECTION_ID&avatar_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "avatar_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uwearai/latest/actions/get-avatar-details?${params}`, {
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
| `avatar_id` | number | yes | Avatar ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "age": 1,
      "avatar_description": "string",
      "avatar_id": 1,
      "avatar_name": "Ava Chen",
      "avatar_url": "https://example.com",
      "body": "string",
      "created_at": "string",
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `age` | number |  |
| `avatar_description` | string |  |
| `avatar_id` | number |  |
| `avatar_name` | string |  |
| `avatar_url` | string |  |
| `body` | string |  |
| `created_at` | string |  |
| `updated_at` | string |  |

## Native endpoint

Through the native Uwear.ai API, this operation is `GET /api/v1/avatar/:avatar_id` (base URL `https://api.uwear.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-avatar-details.md) for the provider-specific parameters and requirements.

