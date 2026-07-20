# SelectPdf: Search PDF File



```
GET https://connect.mindcloud.co/v1/universal/selectPdf/latest/actions/search-pdf-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SelectPdf `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/selectPdf/latest/actions/search-pdf-file?connectionId=$CONNECTION_ID&file=string&searchText=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "file": "string",
  "searchText": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/selectPdf/latest/actions/search-pdf-file?${params}`, {
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
| `file` | file | yes | The PDF file to search. |
| `searchText` | string | yes | Text to search for inside the PDF. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "height": 1,
      "pageNumber": 1,
      "width": 1,
      "x": 1,
      "y": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `height` | number | Height of the matched text region. |
| `pageNumber` | number | Page number where the search match was found. |
| `width` | number | Width of the matched text region. |
| `x` | number | Horizontal coordinate of the search match. |
| `y` | number | Vertical coordinate of the search match. |

## Native endpoint

Through the native SelectPdf API, this operation is `POST /pdftotext/` (base URL `https://selectpdf.com/api2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-pdf-file.md) for the provider-specific parameters and requirements.

