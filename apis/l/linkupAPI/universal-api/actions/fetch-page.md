# LinkupAPI: Fetch Page

Retrieves a single webpage by URL from LinkupAPI.

```
GET https://connect.mindcloud.co/v1/universal/linkupAPI/latest/actions/fetch-page
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LinkupAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/linkupAPI/latest/actions/fetch-page?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/linkupAPI/latest/actions/fetch-page?${params}`, {
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
| `url` | string | yes | The URL of the webpage to fetch. |
| `renderJs` | boolean | no | Render the page's JavaScript before extracting content. Default: `false`. |
| `extractImages` | boolean | no | Extract images from the fetched page. Default: `false`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `includeRawHtml` | boolean | no | Include the raw HTML in the response. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "images": [
        [
          {}
        ]
      ],
      "markdown": "string",
      "rawHtml": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `images[]` | array<object> | Images extracted from the webpage. |
| `images[].alt` | string | The image alt text when available. |
| `images[].url` | string | The image URL. |
| `markdown` | string | The cleaned markdown version of the fetched webpage. |
| `rawHtml` | string | The raw HTML of the fetched webpage. |

## Native endpoint

Through the native LinkupAPI API, this operation is `POST /fetch` (base URL `https://api.linkup.so/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fetch-page.md) for the provider-specific parameters and requirements.

