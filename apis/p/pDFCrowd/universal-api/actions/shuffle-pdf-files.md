# PDFCrowd: Shuffle PDF Files

Creates one PDF by shuffling PDF pages in PDFCrowd.

```
POST https://connect.mindcloud.co/v1/universal/pDFCrowd/latest/actions/shuffle-pdf-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PDFCrowd `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pDFCrowd/latest/actions/shuffle-pdf-files" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "f_1": "string",
  "f_2": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pDFCrowd/latest/actions/shuffle-pdf-files', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "f_1": "string",
    "f_2": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `f_1` | file | yes | First PDF file to shuffle. |
| `f_2` | file | yes | Second PDF file to shuffle. |
| `f_3` | file | no | Optional third PDF file to shuffle. |
| `f_4` | file | no | Optional fourth PDF file to shuffle. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        [
          1
        ]
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
| `data[]` | array<number> |  |
| `type` | string |  |

## Native endpoint

Through the native PDFCrowd API, this operation is `POST https://api.pdfcrowd.com/convert/24.04/` (base URL `https://api.pdfcrowd.com/convert/24.04/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/shuffle-pdf-files.md) for the provider-specific parameters and requirements.

