# Tiledesk: Create Segment

Creates a segment in the current Tiledesk project.

```
POST https://connect.mindcloud.co/v1/universal/tiledesk/latest/actions/create-segment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tiledesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tiledesk/latest/actions/create-segment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tiledesk/latest/actions/create-segment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "createdAt": "string",
      "description": "string",
      "name": "Ava Chen",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string | Unique segment identifier. |
| `createdAt` | string | Creation timestamp. |
| `description` | string | Segment description. |
| `name` | string | Segment name. |
| `updatedAt` | string | Last update timestamp. |

## Native endpoint

Through the native Tiledesk API, this operation is `POST /{{credentials.projectId}}/segments` (base URL `https://api.tiledesk.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-segment.md) for the provider-specific parameters and requirements.

