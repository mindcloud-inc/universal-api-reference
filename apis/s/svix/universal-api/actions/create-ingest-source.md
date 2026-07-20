# Svix: Create Ingest Source

Creates an ingest source in Svix.

```
POST https://connect.mindcloud.co/v1/universal/svix/latest/actions/create-ingest-source
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Svix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/svix/latest/actions/create-ingest-source" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/svix/latest/actions/create-ingest-source', {
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
      "createdAt": "string",
      "id": "string",
      "ingestUrl": "https://example.com",
      "metadata": {},
      "name": "Ava Chen",
      "type": "string",
      "uid": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `id` | string |  |
| `ingestUrl` | string |  |
| `metadata` | object |  |
| `name` | string |  |
| `type` | string |  |
| `uid` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Svix API, this operation is `POST /ingest/api/v1/source` (base URL `https://api.us.svix.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-ingest-source.md) for the provider-specific parameters and requirements.

