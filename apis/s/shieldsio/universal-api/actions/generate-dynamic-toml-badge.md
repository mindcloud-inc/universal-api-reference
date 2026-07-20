# Shields.io: Generate Dynamic TOML Badge

Retrieves a badge image from TOML data in Shields.io.

```
GET https://connect.mindcloud.co/v1/universal/shieldsio/latest/actions/generate-dynamic-toml-badge
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shields.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shieldsio/latest/actions/generate-dynamic-toml-badge?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fraw.githubusercontent.com%2Fsquirrelchat%2Fsmol-toml%2Fmistress%2Fbench%2Ftestfiles%2Ftoml-spec-example.toml&query=%24.title" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://raw.githubusercontent.com/squirrelchat/smol-toml/mistress/bench/testfiles/toml-spec-example.toml",
  "query": "$.title"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shieldsio/latest/actions/generate-dynamic-toml-badge?${params}`, {
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
| `url` | string | yes | URL to a TOML document. Default: `https://raw.githubusercontent.com/squirrelchat/smol-toml/mistress/bench/testfiles/toml-spec-example.toml`. |
| `query` | string | yes | JSONPath expression used to select the badge value. Default: `$.title`. |
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

Through the native Shields.io API, this operation is `GET /badge/dynamic/toml` (base URL `https://img.shields.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-dynamic-toml-badge.md) for the provider-specific parameters and requirements.

