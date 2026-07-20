# Bonusly: List User Achievements

Retrieves achievements for a Bonusly user.

```
GET https://connect.mindcloud.co/v1/universal/bonusly/latest/actions/list-user-achievements
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bonusly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bonusly/latest/actions/list-user-achievements?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bonusly/latest/actions/list-user-achievements?${params}`, {
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
| `id` | string | yes | The Bonusly user ID whose achievements to list. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "description": "string",
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `description` | string |  |
| `id` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Bonusly API, this operation is `GET /users/:id/achievements` (base URL `https://bonus.ly/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-user-achievements.md) for the provider-specific parameters and requirements.

