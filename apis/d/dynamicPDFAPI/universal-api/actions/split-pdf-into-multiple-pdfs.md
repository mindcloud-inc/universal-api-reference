# DynamicPDF: Split PDF Into Multiple PDFs

Splits a PDF into multiple PDFs in DynamicPDF API.

```
GET https://connect.mindcloud.co/v1/universal/dynamicPDFAPI/latest/actions/split-pdf-into-multiple-pdfs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DynamicPDF `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dynamicPDFAPI/latest/actions/split-pdf-into-multiple-pdfs?connectionId=$CONNECTION_ID&instructions=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "instructions": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dynamicPDFAPI/latest/actions/split-pdf-into-multiple-pdfs?${params}`, {
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
| `instructions` | object | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string |  |

## Native endpoint

Through the native DynamicPDF API, this operation is `POST /v1.0/pdf` (base URL `https://api.dpdf.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/split-pdf-into-multiple-pdfs.md) for the provider-specific parameters and requirements.

