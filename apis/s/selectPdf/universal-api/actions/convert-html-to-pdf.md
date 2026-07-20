# SelectPdf: Convert HTML to PDF



```
POST https://connect.mindcloud.co/v1/universal/selectPdf/latest/actions/convert-html-to-pdf
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SelectPdf `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/selectPdf/latest/actions/convert-html-to-pdf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "html": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/selectPdf/latest/actions/convert-html-to-pdf', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "html": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `html` | string | yes | Raw HTML markup to convert into a PDF. |
| `baseUrl` | string | no | Optional base URL used to resolve relative paths inside the HTML markup. |

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
| `data` | array<number> | Binary bytes of the generated PDF file. |
| `type` | string | Runtime payload type for the generated PDF buffer. |

## Native endpoint

Through the native SelectPdf API, this operation is `POST /convert/` (base URL `https://selectpdf.com/api2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert-html-to-pdf.md) for the provider-specific parameters and requirements.

