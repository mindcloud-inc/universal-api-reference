# Cloudmersive Document Conversion: Convert HTML File to PDF

Converts an HTML file to PDF.

```
GET https://connect.mindcloud.co/v1/universal/cloudmersiveDocumentConversion/latest/actions/convert-html-file-to-pdf
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudmersive Document Conversion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudmersiveDocumentConversion/latest/actions/convert-html-file-to-pdf?connectionId=$CONNECTION_ID&inputFile=PGgxPkNsb3VkbWVyc2l2ZSBEb2N1bWVudCBDb252ZXJzaW9uPC9oMT4%3D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "inputFile": "PGgxPkNsb3VkbWVyc2l2ZSBEb2N1bWVudCBDb252ZXJzaW9uPC9oMT4="
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudmersiveDocumentConversion/latest/actions/convert-html-file-to-pdf?${params}`, {
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
| `inputFile` | file | yes | Input HTML document file to convert to PDF. Default: `PGgxPkNsb3VkbWVyc2l2ZSBEb2N1bWVudCBDb252ZXJzaW9uPC9oMT4=`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "outputFile": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `outputFile` | string | Converted PDF file content returned by Cloudmersive. |

## Native endpoint

Through the native Cloudmersive Document Conversion API, this operation is `POST /convert/html/to/pdf` (base URL `https://api.cloudmersive.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert-html-file-to-pdf.md) for the provider-specific parameters and requirements.

