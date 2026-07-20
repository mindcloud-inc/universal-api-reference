# PDF Snake: Impose Document

Creates an imposed document from uploaded files in PDF Snake.

```
POST https://connect.mindcloud.co/v1/universal/pDFSnake/latest/actions/impose-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PDF Snake `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pDFSnake/latest/actions/impose-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "doc": "https://pdfsnake.com/pdf/in.pdf",
  "steps": "W10="
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pDFSnake/latest/actions/impose-document', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "doc": "https://pdfsnake.com/pdf/in.pdf",
    "steps": "W10="
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `doc` | file | yes | The PDF, JPEG, or PNG document to impose. Example: `https://pdfsnake.com/pdf/in.pdf`. |
| `steps` | file | yes | Upload the PDF Snake steps.json file. An empty JSON array (`[]`) is valid for a minimal passthrough imposition. Example: `W10=`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `overlay` | file | no | Optional overlay PDF used when the steps.json contains an Overlay step. Example: `https://example.com/overlay.pdf`. |
| `insert` | file | no | Optional insert PDF used when the steps.json contains an Insert Pages step. Example: `https://example.com/insert.pdf`. |

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
| `data` | array<number> | Byte array for the imposed PDF file returned by PDF Snake. |
| `type` | string | Node-style buffer type marker returned for the imposed file payload. |

## Native endpoint

Through the native PDF Snake API, this operation is `POST /impose` (base URL `https://api2.pdfsnake.app/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/impose-document.md) for the provider-specific parameters and requirements.

