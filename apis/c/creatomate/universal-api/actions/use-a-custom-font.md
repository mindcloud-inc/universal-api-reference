# Creatomate: Use A Custom Font

Creates a render that uses a custom font.

```
POST https://connect.mindcloud.co/v1/universal/creatomate/latest/actions/use-a-custom-font
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Creatomate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/creatomate/latest/actions/use-a-custom-font" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fontFamily": "Coolvetica Rg",
  "regularFontUrl": "https://cdn.creatomate.com/demo/coolvetica-rg.otf",
  "headlineText": "Hello, world!"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/creatomate/latest/actions/use-a-custom-font', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fontFamily": "Coolvetica Rg",
    "regularFontUrl": "https://cdn.creatomate.com/demo/coolvetica-rg.otf",
    "headlineText": "Hello, world!"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fontFamily` | string | yes | Font family name to register and use in the render. Default: `Coolvetica Rg`. |
| `regularFontUrl` | string | yes | URL for the regular font file. Example: `https://cdn.creatomate.com/demo/coolvetica-rg.otf`. |
| `headlineText` | string | yes | Primary text rendered with the custom font. Example: `Hello, world!`. |
| `subheadlineText` | string | no | Optional secondary text line rendered below the headline. Example: `This uses your custom font.`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `italicFontUrl` | string | no | Optional URL for the italic font file. Example: `https://cdn.creatomate.com/demo/coolvetica-rg-it.otf`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "outputFormat": "string",
      "status": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Creatomate render ID. |
| `outputFormat` | string | Output format requested for the render. |
| `status` | string | Current render status returned by Creatomate. |
| `url` | string | Direct URL for the rendered output file. |

## Native endpoint

Through the native Creatomate API, this operation is `POST /v2/renders` (base URL `https://api.creatomate.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/use-a-custom-font.md) for the provider-specific parameters and requirements.

