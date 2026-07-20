# Veryfi OCR: Process W-8BEN-E

Processes a W-8BEN-E in Veryfi OCR.

```
POST https://connect.mindcloud.co/v1/universal/veryfiOCR/latest/actions/process-w8ben-e
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Veryfi OCR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/veryfiOCR/latest/actions/process-w8ben-e" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/veryfiOCR/latest/actions/process-w8ben-e', {
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
      "id": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Veryfi OCR API, this operation is `POST /api/v8/partner/w-8ben-e` (base URL `https://api.veryfi.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/process-w8ben-e.md) for the provider-specific parameters and requirements.

