# Shields.io: Generate Static Badge

Retrieves a custom static badge image from Shields.io.

```
GET https://connect.mindcloud.co/v1/universal/shieldsio/latest/actions/generate-static-badge
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shields.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shieldsio/latest/actions/generate-static-badge?connectionId=$CONNECTION_ID&badgeContent=build-passing-brightgreen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "badgeContent": "build-passing-brightgreen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shieldsio/latest/actions/generate-static-badge?${params}`, {
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
| `badgeContent` | string | yes | Path content for the badge, encoded as label-message-color or message-color separated by dashes. Default: `build-passing-brightgreen`. |
| `style` | string | no | Badge style. Supported values include flat, flat-square, plastic, for-the-badge, and social. Default: `flat`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `logo` | string | no | Simple Icons slug for an optional badge logo. |
| `label` | string | no | Override the badge left-side label text. |

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

Through the native Shields.io API, this operation is `GET /badge/:badgeContent` (base URL `https://img.shields.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-static-badge.md) for the provider-specific parameters and requirements.

