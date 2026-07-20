# ManyChat: Remove Tag From Subscriber By Name

Removes a tag from a subscriber in ManyChat by name.

```
PUT https://connect.mindcloud.co/v1/universal/manyChat/latest/actions/remove-tag-from-subscriber-by-name
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ManyChat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/manyChat/latest/actions/remove-tag-from-subscriber-by-name" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "subscriber_id": 1,
  "tag_name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/manyChat/latest/actions/remove-tag-from-subscriber-by-name', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "subscriber_id": 1,
    "tag_name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `subscriber_id` | number | yes |  |
| `tag_name` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string |  |

## Native endpoint

Through the native ManyChat API, this operation is `POST /fb/subscriber/removeTagByName` (base URL `https://api.manychat.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-tag-from-subscriber-by-name.md) for the provider-specific parameters and requirements.

