# PDF API Hub: Extract Text From File



```
GET https://connect.mindcloud.co/v1/universal/pDFAPIHub/latest/actions/extract-text-from-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PDF API Hub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pDFAPIHub/latest/actions/extract-text-from-file?connectionId=$CONNECTION_ID&file=https%3A%2F%2Fwww.adobe.com%2Fsupport%2Fproducts%2Fenterprise%2Fknowledgecenter%2Fmedia%2Fc4611_sample_explain.pdf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "file": "https://www.adobe.com/support/products/enterprise/knowledgecenter/media/c4611_sample_explain.pdf"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pDFAPIHub/latest/actions/extract-text-from-file?${params}`, {
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
| `file` | file | yes | PDF file upload; can also be a public PDF URL Default: `https://www.adobe.com/support/products/enterprise/knowledgecenter/media/c4611_sample_explain.pdf`. |
| `inline` | boolean | no | Return text inline instead of file Default: `false`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native PDF API Hub API returns.

## Native endpoint

Through the native PDF API Hub API, this operation is `POST /extract-text` (base URL `https://api.prefillpdf.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/extract-text-from-file.md) for the provider-specific parameters and requirements.

