# CustomJS: Convert Markdown to PDF

Converts Markdown to a PDF in CustomJS.

```
POST https://connect.mindcloud.co/v1/universal/customJS/latest/actions/convert-markdown-to-pdf
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CustomJS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/customJS/latest/actions/convert-markdown-to-pdf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "input.markdown": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/customJS/latest/actions/convert-markdown-to-pdf', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "input.markdown": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `input.markdown` | string | yes | Markdown content to convert to PDF. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        1
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[]` | number |  |
| `type` | string |  |

## Native endpoint

Through the native CustomJS API, this operation is `POST https://e.customjs.io/markdown2pdf` (base URL `https://e.customjs.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert-markdown-to-pdf.md) for the provider-specific parameters and requirements.

