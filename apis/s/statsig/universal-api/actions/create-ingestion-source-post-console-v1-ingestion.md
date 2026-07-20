# Statsig: Create Ingestion Source

Creates an ingestion source in Statsig.

```
POST https://connect.mindcloud.co/v1/universal/statsig/latest/actions/create-ingestion-source-post-console-v1-ingestion
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Statsig `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/statsig/latest/actions/create-ingestion-source-post-console-v1-ingestion" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/statsig/latest/actions/create-ingestion-source-post-console-v1-ingestion', {
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
      "data": {},
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Statsig response data payload. |
| `message` | string | Statsig response message. |

## Native endpoint

Through the native Statsig API, this operation is `POST /console/v1/ingestion` (base URL `https://statsigapi.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-ingestion-source-post-console-v1-ingestion.md) for the provider-specific parameters and requirements.

