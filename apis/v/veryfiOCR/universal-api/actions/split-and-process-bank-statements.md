# Veryfi OCR: Split And Process Bank Statements

Processes split bank statements in Veryfi OCR.

```
POST https://connect.mindcloud.co/v1/universal/veryfiOCR/latest/actions/split-and-process-bank-statements
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Veryfi OCR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/veryfiOCR/latest/actions/split-and-process-bank-statements" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/veryfiOCR/latest/actions/split-and-process-bank-statements', {
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

Through the native Veryfi OCR API, this operation is `POST /api/v8/partner/bank-statements-set` (base URL `https://api.veryfi.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/split-and-process-bank-statements.md) for the provider-specific parameters and requirements.

