# Nutrient Document Converter: Convert Markdown to PDF

Converts Markdown to PDF in Nutrient.

```
GET https://connect.mindcloud.co/v1/universal/nutrientDocumentConverter/latest/actions/convert-markdown-to-pdf
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nutrient Document Converter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nutrientDocumentConverter/latest/actions/convert-markdown-to-pdf?connectionId=$CONNECTION_ID&markdown=%23%20Hello%20from%20Nutrient%5Cn%5CnThis%20PDF%20was%20generated%20from%20Markdown." \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "markdown": "# Hello from Nutrient\\n\\nThis PDF was generated from Markdown."
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nutrientDocumentConverter/latest/actions/convert-markdown-to-pdf?${params}`, {
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
| `markdown` | string | yes | Markdown content to convert into a PDF. Default: `# Hello from Nutrient\\n\\nThis PDF was generated from Markdown.`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `template` | string | no | Optional built-in template such as built-in:corporate. Default: `built-in:default`. |
| `css` | string | no | Optional CSS overrides for the PDF output. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contentType": "string",
      "outputFile": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contentType` | string | Response content type. |
| `outputFile` | string | Generated PDF binary response. |

## Native endpoint

Through the native Nutrient Document Converter API, this operation is `POST /processor/md_to_pdf` (base URL `https://api.nutrient.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert-markdown-to-pdf.md) for the provider-specific parameters and requirements.

