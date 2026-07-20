# Uwear.ai: Update Avatar

Updates an existing avatar in Uwear.ai.

```
PUT https://connect.mindcloud.co/v1/universal/uwearai/latest/actions/update-avatar
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Uwear.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/uwearai/latest/actions/update-avatar" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "avatar_id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/uwearai/latest/actions/update-avatar', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "avatar_id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `avatar_description` | string | no | Updated avatar description. |
| `avatar_id` | number | yes | Avatar ID. |
| `avatar_name` | string | no | Updated avatar name. |

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

Through the native Uwear.ai API, this operation is `PUT /api/v1/avatar/:avatar_id` (base URL `https://api.uwear.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-avatar.md) for the provider-specific parameters and requirements.

