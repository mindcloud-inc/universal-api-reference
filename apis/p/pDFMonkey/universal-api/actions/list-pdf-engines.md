# PDFMonkey: List PDF Engines

Retrieves PDF engines from PDFMonkey.

```
GET https://connect.mindcloud.co/v1/universal/pDFMonkey/latest/actions/list-pdf-engines
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PDFMonkey `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pDFMonkey/latest/actions/list-pdf-engines?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pDFMonkey/latest/actions/list-pdf-engines?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "pdfEngine": {
        "deprecatedOn": "2026-05-07T12:00:00.000Z",
        "id": "string",
        "name": "Ava Chen",
        "version": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pdfEngine.deprecatedOn` | date | Deprecation date when present. |
| `pdfEngine.id` | string | PDF engine ID. |
| `pdfEngine.name` | string | PDF engine name. |
| `pdfEngine.version` | number | Engine version number. |

## Native endpoint

Through the native PDFMonkey API, this operation is `GET /pdf_engines` (base URL `https://api.pdfmonkey.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-pdf-engines.md) for the provider-specific parameters and requirements.

