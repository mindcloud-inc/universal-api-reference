# Circle: Update Member Tag

Updates an existing member tag in Circle.

```
PUT https://connect.mindcloud.co/v1/universal/circle/latest/actions/update-member-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Circle `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/circle/latest/actions/update-member-tag" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/circle/latest/actions/update-member-tag', {
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
| `id` | number | yes | Member tag ID |
| `name` | string | no | Member tag name |
| `displayFormat` | list | no | Display format One of: `icon`, `label`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "color": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customEmojiDarkUrl": "https://example.com",
      "customEmojiUrl": "https://example.com",
      "displayFormat": "string",
      "displayLocations": "string",
      "emoji": "string",
      "id": 1,
      "isBackgroundEnabled": true,
      "isPublic": true,
      "name": "Ava Chen",
      "taggedMembersCount": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | string |  |
| `createdAt` | date |  |
| `customEmojiDarkUrl` | string |  |
| `customEmojiUrl` | string |  |
| `displayFormat` | string |  |
| `displayLocations` | string |  |
| `emoji` | string |  |
| `id` | number |  |
| `isBackgroundEnabled` | boolean |  |
| `isPublic` | boolean |  |
| `name` | string |  |
| `taggedMembersCount` | number |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Circle API, this operation is `PUT /api/admin/v2/member_tags/[:id]` (base URL `https://{{credentials.subdomain}}.circle.so`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-member-tag.md) for the provider-specific parameters and requirements.

