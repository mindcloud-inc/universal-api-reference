# QuickFile: Get Invoice PDF



```
GET https://connect.mindcloud.co/v1/universal/quickFile/latest/actions/get-invoice-pdf
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QuickFile `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quickFile/latest/actions/get-invoice-pdf?connectionId=$CONNECTION_ID&invoiceId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "invoiceId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quickFile/latest/actions/get-invoice-pdf?${params}`, {
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
| `invoiceId` | number | yes | Default: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "invoiceId": 1,
      "pdfUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `invoiceId` | number |  |
| `pdfUrl` | string |  |

## Native endpoint

Through the native QuickFile API, this operation is `POST /invoice/getpdf` (base URL `https://api.quickfile.co.uk/1_2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-invoice-pdf.md) for the provider-specific parameters and requirements.

