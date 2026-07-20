# WiseOCR: Extract Receipt Data From URL

Retrieves extracted receipt data from WiseOCR using a file URL.

```
GET https://connect.mindcloud.co/v1/universal/wiseOCR/latest/actions/extract-receipt-data-from-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WiseOCR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wiseOCR/latest/actions/extract-receipt-data-from-url?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com%2Fpath%2Fto%2Freceipt.jpg" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com/path/to/receipt.jpg"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wiseOCR/latest/actions/extract-receipt-data-from-url?${params}`, {
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
| `url` | string | yes | URL of the receipt image or PDF file Example: `https://example.com/path/to/receipt.jpg`. |
| `skipItems` | boolean | no | Skip detailed line item extraction to speed up processing Example: `false`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native WiseOCR API returns.

## Native endpoint

Through the native WiseOCR API, this operation is `POST /url` (base URL `https://api.wiseocr.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/extract-receipt-data-from-url.md) for the provider-specific parameters and requirements.

