# Shields.io: Generate Dynamic Regex Badge

Retrieves a badge image from regex-matched text in Shields.io.

```
GET https://connect.mindcloud.co/v1/universal/shieldsio/latest/actions/generate-dynamic-regex-badge
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shields.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shieldsio/latest/actions/generate-dynamic-regex-badge?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fraw.githubusercontent.com%2Fbadges%2Fshields%2Fmaster%2FREADME.md&search=Every%20(.*%3F)%20it%20serves%20(%3F%3Camount%3E.*%3F)%20images" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://raw.githubusercontent.com/badges/shields/master/README.md",
  "search": "Every (.*?) it serves (?<amount>.*?) images"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shieldsio/latest/actions/generate-dynamic-regex-badge?${params}`, {
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
| `url` | string | yes | URL to a text file to search. Default: `https://raw.githubusercontent.com/badges/shields/master/README.md`. |
| `search` | string | yes | RE2 expression used to extract badge text from the document. Default: `Every (.*?) it serves (?<amount>.*?) images`. |
| `replace` | string | no | Optional replacement string for the regex match. Default: `$<amount>`. |
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

Through the native Shields.io API, this operation is `GET /badge/dynamic/regex` (base URL `https://img.shields.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-dynamic-regex-badge.md) for the provider-specific parameters and requirements.

