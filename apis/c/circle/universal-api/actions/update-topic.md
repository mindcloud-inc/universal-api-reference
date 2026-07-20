# Circle: Update Topic

Updates an existing topic in Circle.

```
PUT https://connect.mindcloud.co/v1/universal/circle/latest/actions/update-topic
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Circle `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/circle/latest/actions/update-topic" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/circle/latest/actions/update-topic', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Topic ID |
| `name` | string | no | Topic name |
| `adminOnly` | boolean | no | Admin only toggle |
| `spaceIds[]` | array<number> | no | Space IDs |

## Response

```json
{
  "success": true,
  "data": [
    {
      "adminOnly": true,
      "author": {
        "avatarUrl": "https://example.com",
        "firstName": "Ava",
        "lastName": "Chen"
      },
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "name": "Ava Chen",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `adminOnly` | boolean |  |
| `author.avatarUrl` | string |  |
| `author.firstName` | string |  |
| `author.lastName` | string |  |
| `createdAt` | date |  |
| `id` | number |  |
| `name` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Circle API, this operation is `PUT /api/admin/v2/topics/[:id]` (base URL `https://{{credentials.subdomain}}.circle.so`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-topic.md) for the provider-specific parameters and requirements.

