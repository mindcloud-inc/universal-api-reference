# Campfire: List Entity Access



```
GET https://connect.mindcloud.co/v1/universal/campfire/latest/actions/list-entity-access
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Campfire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/campfire/latest/actions/list-entity-access?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/campfire/latest/actions/list-entity-access?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "created_by": 1,
      "created_by_email": "ava@example.com",
      "entity": 1,
      "entity_name": "Ava Chen",
      "id": 1,
      "user": 1,
      "user_email": "ava@example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date |  |
| `created_by` | number |  |
| `created_by_email` | string |  |
| `entity` | number |  |
| `entity_name` | string |  |
| `id` | number |  |
| `user` | number |  |
| `user_email` | string |  |

## Native endpoint

Through the native Campfire API, this operation is `GET /users/api/entity-access/` (base URL `https://api.meetcampfire.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-entity-access.md) for the provider-specific parameters and requirements.

