# PDF API Hub: Extract Text From URL



```
GET https://connect.mindcloud.co/v1/universal/pDFAPIHub/latest/actions/extract-text-from-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PDF API Hub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pDFAPIHub/latest/actions/extract-text-from-url?connectionId=$CONNECTION_ID&fileUrl=https%3A%2F%2Fwww.adobe.com%2Fsupport%2Fproducts%2Fenterprise%2Fknowledgecenter%2Fmedia%2Fc4611_sample_explain.pdf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileUrl": "https://www.adobe.com/support/products/enterprise/knowledgecenter/media/c4611_sample_explain.pdf"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pDFAPIHub/latest/actions/extract-text-from-url?${params}`, {
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
| `fileUrl` | string | yes | Public or signed PDF URL to download. Default: `https://www.adobe.com/support/products/enterprise/knowledgecenter/media/c4611_sample_explain.pdf`. |
| `inline` | boolean | no | Return text inline instead of a file. Default: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "filename": "Ava Chen",
      "metadata": {},
      "pages": 1,
      "source": "string",
      "text": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `filename` | string | Filename derived from the source PDF URL. |
| `metadata` | object | Provider metadata about the extraction output. |
| `pages` | number | Number of pages detected in the PDF. |
| `source` | string | Input source type used by the provider. |
| `text` | string | Extracted text content with page markers when inline text is returned. |

## Native endpoint

Through the native PDF API Hub API, this operation is `POST /extract-text-from-url` (base URL `https://api.prefillpdf.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/extract-text-from-url.md) for the provider-specific parameters and requirements.

