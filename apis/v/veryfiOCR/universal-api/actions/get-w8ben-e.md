# Veryfi OCR: Get W-8BEN-E

Retrieves a W-8BEN-E from Veryfi OCR.

```
GET https://connect.mindcloud.co/v1/universal/veryfiOCR/latest/actions/get-w8ben-e
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Veryfi OCR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/veryfiOCR/latest/actions/get-w8ben-e?connectionId=$CONNECTION_ID&documentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "documentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/veryfiOCR/latest/actions/get-w8ben-e?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `documentId` | string | yes | The Veryfi document identifier. |

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

Through the native Veryfi OCR API, this operation is `GET /api/v8/partner/w-8ben-e/:document_id` (base URL `https://api.veryfi.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-w8ben-e.md) for the provider-specific parameters and requirements.

