# Circle: Create Community Segment

Creates a new community segment in Circle.

```
POST https://connect.mindcloud.co/v1/universal/circle/latest/actions/create-community-segment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Circle `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/circle/latest/actions/create-community-segment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string",
  "visible": true,
  "rules": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/circle/latest/actions/create-community-segment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string",
    "visible": true,
    "rules": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | yes | Community segment title |
| `visible` | boolean | yes | Segment visibility flag |
| `rules` | object | yes | Segment rules object |

## Response

```json
{
  "success": true,
  "data": [
    {
      "audienceCount": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": {
        "avatarUrl": "https://example.com",
        "email": "ava@example.com",
        "id": 1,
        "name": "Ava Chen",
        "publicUid": "string"
      },
      "id": 1,
      "rules": {
        "ruleType": "string"
      },
      "title": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "visible": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `audienceCount` | number |  |
| `createdAt` | date |  |
| `createdBy.avatarUrl` | string |  |
| `createdBy.email` | string |  |
| `createdBy.id` | number |  |
| `createdBy.name` | string |  |
| `createdBy.publicUid` | string |  |
| `id` | number |  |
| `rules.ruleType` | string |  |
| `title` | string |  |
| `updatedAt` | date |  |
| `visible` | boolean |  |

## Native endpoint

Through the native Circle API, this operation is `POST /api/admin/v2/community_segments` (base URL `https://{{credentials.subdomain}}.circle.so`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-community-segment.md) for the provider-specific parameters and requirements.

