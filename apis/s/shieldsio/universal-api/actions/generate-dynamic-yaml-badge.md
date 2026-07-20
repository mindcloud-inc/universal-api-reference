# Shields.io: Generate Dynamic YAML Badge

Retrieves a badge image from YAML data in Shields.io.

```
GET https://connect.mindcloud.co/v1/universal/shieldsio/latest/actions/generate-dynamic-yaml-badge
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shields.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shieldsio/latest/actions/generate-dynamic-yaml-badge?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fraw.githubusercontent.com%2Fbadges%2Fshields%2Fmaster%2F.github%2Fdependabot.yml&query=%24.version" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://raw.githubusercontent.com/badges/shields/master/.github/dependabot.yml",
  "query": "$.version"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shieldsio/latest/actions/generate-dynamic-yaml-badge?${params}`, {
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
| `url` | string | yes | URL to a YAML document. Default: `https://raw.githubusercontent.com/badges/shields/master/.github/dependabot.yml`. |
| `query` | string | yes | JSONPath expression used to select the badge value. Default: `$.version`. |
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

Through the native Shields.io API, this operation is `GET /badge/dynamic/yaml` (base URL `https://img.shields.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-dynamic-yaml-badge.md) for the provider-specific parameters and requirements.

