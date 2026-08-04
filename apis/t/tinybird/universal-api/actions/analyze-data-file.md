# Tinybird: Analyze Data File



```
POST https://connect.mindcloud.co/v1/universal/tinybird/latest/actions/analyze-data-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tinybird `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tinybird/latest/actions/analyze-data-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tinybird/latest/actions/analyze-data-file', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | Remote CSV, NDJSON, or Parquet file URL to analyze |

## Response

```json
{
  "success": true,
  "data": [
    {
      "analysis": {},
      "dialect": {},
      "preview": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `analysis` | object |  |
| `dialect` | object |  |
| `preview` | array<object> |  |

## Native endpoint

Through the native Tinybird API, this operation is `POST v0/analyze` (base URL `{{credentials.apiHost}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/analyze-data-file.md) for the provider-specific parameters and requirements.

