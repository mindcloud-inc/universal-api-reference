# Socialbu: List Queues

Retrieves publishing queues from SocialBu.

```
GET https://connect.mindcloud.co/v1/universal/socialbu/latest/actions/list-queues
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Socialbu `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/socialbu/latest/actions/list-queues?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/socialbu/latest/actions/list-queues?${params}`, {
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
      "active": true,
      "id": 1,
      "name": "Ava Chen",
      "next_publish_at": "string",
      "team_id": 1,
      "times_to_publish": 1,
      "user_id": 1,
      "user_name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `id` | number |  |
| `name` | string |  |
| `next_publish_at` | string |  |
| `team_id` | number |  |
| `times_to_publish` | number |  |
| `user_id` | number |  |
| `user_name` | string |  |

## Native endpoint

Through the native Socialbu API, this operation is `GET /queues` (base URL `https://socialbu.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-queues.md) for the provider-specific parameters and requirements.

