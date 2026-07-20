# SelectPdf: Merge PDFs from URLs



```
POST https://connect.mindcloud.co/v1/universal/selectPdf/latest/actions/merge-pd-fs-from-ur-ls
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SelectPdf `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/selectPdf/latest/actions/merge-pd-fs-from-ur-ls" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url1": "https://example.com",
  "url2": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/selectPdf/latest/actions/merge-pd-fs-from-ur-ls', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url1": "https://example.com",
    "url2": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url1` | string | yes | The first public PDF URL to merge. |
| `url2` | string | yes | The second public PDF URL to merge. |

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
| `data` | array<number> | Binary bytes of the merged PDF file. |
| `type` | string | Runtime payload type for the merged PDF buffer. |

## Native endpoint

Through the native SelectPdf API, this operation is `POST /pdfmerge/` (base URL `https://selectpdf.com/api2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/merge-pd-fs-from-ur-ls.md) for the provider-specific parameters and requirements.

