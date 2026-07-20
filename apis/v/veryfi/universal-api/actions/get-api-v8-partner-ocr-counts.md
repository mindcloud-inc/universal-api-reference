# Veryfi: Get ocr-counts

Retrieves OCR counts from Veryfi.

```
GET https://connect.mindcloud.co/v1/universal/veryfi/latest/actions/get-api-v8-partner-ocr-counts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Veryfi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/veryfi/latest/actions/get-api-v8-partner-ocr-counts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/veryfi/latest/actions/get-api-v8-partner-ocr-counts?${params}`, {
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
| `ocrType` | string<string> | no | Possible values: [ pepsico_codes , pepsico_caps ] Default value: pepsico_codes OCR type |
| `createdDateGt` | string | no | Created date filter greater than. |
| `createdDateLt` | string | no | Created date filter lower than. |
| `createdDateGte` | string | no | Created date filter greater or equal. |
| `createdDateLte` | string | no | Created date filter lower or equal. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "number_of_scans": 1,
      "source": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `number_of_scans` | number |  |
| `source` | string |  |

## Native endpoint

Through the native Veryfi API, this operation is `GET /api/v8/partner/ocr-counts` (base URL `https://api.veryfi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-api-v8-partner-ocr-counts.md) for the provider-specific parameters and requirements.

