# Shields.io: Generate Dynamic XML Badge

Retrieves a badge image from XML data in Shields.io.

```
GET https://connect.mindcloud.co/v1/universal/shieldsio/latest/actions/generate-dynamic-xml-badge
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shields.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shieldsio/latest/actions/generate-dynamic-xml-badge?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fhttpbin.org%2Fxml&query=%2F%2Fslideshow%2Fslide%5B1%5D%2Ftitle" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://httpbin.org/xml",
  "query": "//slideshow/slide[1]/title"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shieldsio/latest/actions/generate-dynamic-xml-badge?${params}`, {
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
| `url` | string | yes | URL to an XML document. Default: `https://httpbin.org/xml`. |
| `query` | string | yes | XPath expression used to select the badge value. Default: `//slideshow/slide[1]/title`. |
| `style` | string | no | Badge style. Supported values include flat, flat-square, plastic, for-the-badge, and social. Default: `flat`. |

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
| `data` | array<number> | Raw SVG image bytes returned by Shields.io. |
| `type` | string | Raw response object type, usually Buffer for badge image data. |

## Native endpoint

Through the native Shields.io API, this operation is `GET /badge/dynamic/xml` (base URL `https://img.shields.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-dynamic-xml-badge.md) for the provider-specific parameters and requirements.

