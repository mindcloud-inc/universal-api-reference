# SelectPdf: Search PDF URL



```
GET https://connect.mindcloud.co/v1/universal/selectPdf/latest/actions/search-pdfurl
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SelectPdf `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/selectPdf/latest/actions/search-pdfurl?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com&searchText=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com",
  "searchText": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/selectPdf/latest/actions/search-pdfurl?${params}`, {
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
| `url` | string | yes | The public PDF URL to search. |
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

Through the native SelectPdf API, this operation is `POST /pdftotext/` (base URL `https://selectpdf.com/api2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-pdfurl.md) for the provider-specific parameters and requirements.

