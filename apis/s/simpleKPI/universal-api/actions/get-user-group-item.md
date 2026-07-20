# SimpleKPI: Get User Group Item

Retrieves a user's group item from SimpleKPI.

```
GET https://connect.mindcloud.co/v1/universal/simpleKPI/latest/actions/get-user-group-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SimpleKPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simpleKPI/latest/actions/get-user-group-item?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simpleKPI/latest/actions/get-user-group-item?${params}`, {
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
| `id` | number | no | The group item ID assigned to the user. |
| `userId` | number | no | The user ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "group_id": 1,
      "group_name": "Ava Chen",
      "id": 1,
      "name": "Ava Chen",
      "user_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string |  |
| `group_id` | number |  |
| `group_name` | string |  |
| `id` | number |  |
| `name` | string |  |
| `user_id` | number |  |

## Native endpoint

Through the native SimpleKPI API, this operation is `GET users/:userId/groupitems/:id` (base URL `https://{{credentials.subdomain}}.simplekpi.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-group-item.md) for the provider-specific parameters and requirements.

