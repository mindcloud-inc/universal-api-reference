# Duply: Generate Image

Creates a generated image from a Duply template.

```
POST https://connect.mindcloud.co/v1/universal/duply/latest/actions/generate-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Duply `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/duply/latest/actions/generate-image" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "templateId": "string",
  "formats[]": [
    "string"
  ],
  "fill": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/duply/latest/actions/generate-image', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "templateId": "string",
    "formats[]": ["string"],
    "fill": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `templateId` | string | yes | The ID of the template to generate from. |
| `formats[]` | array<string> | yes | Image output formats to generate, such as jpg, png, or thumb. |
| `fill` | object | yes | Template element values keyed by the element name. |
| `requestName` | string | no | Optional identifier for the generation request. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `transparent` | string | no | Optional transparency flag used when generating png output. |
| `variantName` | string | no | Optional template variant name. Defaults to the oldest variant when omitted. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "announcement": "string",
      "files": [
        {
          "filepath": "string",
          "format": "string",
          "size": 1
        }
      ],
      "id": "string",
      "templateId": "string",
      "urls": {
        "filepathJPG": "https://example.com"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `announcement` | string |  |
| `files[].filepath` | string |  |
| `files[].format` | string |  |
| `files[].size` | number |  |
| `id` | string |  |
| `templateId` | string |  |
| `urls.filepathJPG` | string |  |

## Native endpoint

Through the native Duply API, this operation is `POST /generate/` (base URL `https://gen.duply.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-image.md) for the provider-specific parameters and requirements.

