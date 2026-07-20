# Svix: Create Ingest Endpoint

Creates an ingest endpoint in Svix.

```
POST https://connect.mindcloud.co/v1/universal/svix/latest/actions/create-ingest-endpoint
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Svix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/svix/latest/actions/create-ingest-endpoint" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/svix/latest/actions/create-ingest-endpoint', {
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
      "description": "string",
      "disabled": true,
      "id": "string",
      "metadata": {},
      "rateLimit": 1,
      "uid": "string",
      "updatedAt": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `description` | string |  |
| `disabled` | boolean |  |
| `id` | string |  |
| `metadata` | object |  |
| `rateLimit` | number |  |
| `uid` | string |  |
| `updatedAt` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Svix API, this operation is `POST /ingest/api/v1/source/{source_id}/endpoint` (base URL `https://api.us.svix.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-ingest-endpoint.md) for the provider-specific parameters and requirements.

