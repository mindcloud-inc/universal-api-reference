# Parallel Web Systems: Extract



```
POST https://connect.mindcloud.co/v1/universal/parallelWebSystems/latest/actions/extract
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Parallel Web Systems `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/parallelWebSystems/latest/actions/extract" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/parallelWebSystems/latest/actions/extract', {
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
      "errors": {
        "error_type": "string",
        "url": "https://example.com"
      },
      "extract_id": "string",
      "results": {
        "excerpts": "string",
        "publish_date": "2026-05-07T12:00:00.000Z",
        "title": "string",
        "url": "https://example.com"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errors.error_type` | string | Extraction error type. |
| `errors.url` | string | Errored URL. |
| `extract_id` | string | Extraction identifier. |
| `results.excerpts` | string | Relevant excerpts. |
| `results.publish_date` | date | Published date. |
| `results.title` | string | Result title. |
| `results.url` | string | Source URL. |

## Native endpoint

Through the native Parallel Web Systems API, this operation is `POST /v1beta/extract` (base URL `https://api.parallel.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/extract.md) for the provider-specific parameters and requirements.

