# WiseOCR: Extract Receipt Data From File

Retrieves extracted receipt data from WiseOCR using an uploaded file.

```
GET https://connect.mindcloud.co/v1/universal/wiseOCR/latest/actions/extract-receipt-data-from-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WiseOCR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wiseOCR/latest/actions/extract-receipt-data-from-file?connectionId=$CONNECTION_ID&file=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "file": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wiseOCR/latest/actions/extract-receipt-data-from-file?${params}`, {
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
| `file` | file | yes | Receipt image or PDF file |
| `skipItems` | boolean | no | Skip detailed line item extraction to speed up processing Example: `false`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native WiseOCR API returns.

## Native endpoint

Through the native WiseOCR API, this operation is `POST /file` (base URL `https://api.wiseocr.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/extract-receipt-data-from-file.md) for the provider-specific parameters and requirements.

