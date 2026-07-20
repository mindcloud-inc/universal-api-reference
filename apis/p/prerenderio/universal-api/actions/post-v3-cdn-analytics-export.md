# Prerender.io: Create Cdn Analytics Export

Creates a CDN analytics export in Prerender.io.

```
POST https://connect.mindcloud.co/v1/universal/prerenderio/latest/actions/post-v3-cdn-analytics-export
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Prerender.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/prerenderio/latest/actions/post-v3-cdn-analytics-export" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fileType": "string",
  "interval": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/prerenderio/latest/actions/post-v3-cdn-analytics-export', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fileType": "string",
    "interval": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `adaptive_type` | string | no |  |
| `cacheHit` | string | no |  |
| `fileType` | string | yes |  |
| `interval` | string | yes |  |
| `q` | string | no |  |
| `qCondition` | string | no |  |
| `renderedTimeHigh` | number | no |  |
| `renderedTimeLow` | number | no |  |
| `responseTimeHigh` | number | no |  |
| `responseTimeLow` | number | no |  |
| `sort` | string | no |  |
| `sortDirection` | string | no |  |
| `statusCodeEq` | number | no |  |
| `statusCodeHigh` | number | no |  |
| `statusCodeLow` | number | no |  |
| `timedout` | boolean | no |  |
| `userAgent` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | object |  |

## Native endpoint

Through the native Prerender.io API, this operation is `POST /v3/cdn-analytics-export` (base URL `https://api.prerender.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/post-v3-cdn-analytics-export.md) for the provider-specific parameters and requirements.

