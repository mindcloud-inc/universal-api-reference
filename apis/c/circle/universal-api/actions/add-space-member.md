# Circle: Add Space Member

Creates a new space membership in Circle.

```
POST https://connect.mindcloud.co/v1/universal/circle/latest/actions/add-space-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Circle `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/circle/latest/actions/add-space-member" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "spaceId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/circle/latest/actions/add-space-member', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "spaceId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | Email address to add to the space |
| `spaceId` | list<number> | yes | Target space ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Circle API, this operation is `POST /api/admin/v2/space_members` (base URL `https://{{credentials.subdomain}}.circle.so`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-space-member.md) for the provider-specific parameters and requirements.

