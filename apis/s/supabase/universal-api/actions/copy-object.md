# Supabase: Copy Object

Copies an object between paths in Supabase storage.

```
POST https://connect.mindcloud.co/v1/universal/supabase/latest/actions/copy-object
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Supabase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/supabase/latest/actions/copy-object" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/supabase/latest/actions/copy-object', {
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
      "bucketId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "key": "string",
      "lastAccessedAt": "2026-05-07T12:00:00.000Z",
      "metadata": {},
      "name": "Ava Chen",
      "owner": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "userMetadata": {},
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bucketId` | string |  |
| `createdAt` | date |  |
| `id` | string |  |
| `key` | string |  |
| `lastAccessedAt` | date |  |
| `metadata` | object |  |
| `name` | string |  |
| `owner` | string |  |
| `updatedAt` | date |  |
| `userMetadata` | object |  |
| `version` | string |  |

## Native endpoint

Through the native Supabase API, this operation is `POST /storage/v1/object/copy` (base URL `{{credentials.projectUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/copy-object.md) for the provider-specific parameters and requirements.

