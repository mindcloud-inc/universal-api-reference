# Stripo: Export Template as HTML

Exports a template as an HTML file from Stripo.

```
GET https://connect.mindcloud.co/v1/universal/stripo/latest/actions/export-template-as-html
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stripo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stripo/latest/actions/export-template-as-html?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stripo/latest/actions/export-template-as-html?${params}`, {
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
| `id` | number | yes | The template ID. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `asAmp` | boolean | no | Return AMPHTML code. |
| `includeTranslationVersions` | boolean | no | Include translated versions in the export. |
| `minimize` | boolean | no | Compress the template output. |
| `setImageSizes` | boolean | no | Enable bidimensional image sizes. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "file": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `file` | string | Exported template HTML file content returned by Stripo. |

## Native endpoint

Through the native Stripo API, this operation is `GET /export/html/templates/:id` (base URL `https://my.stripo.email/emailgeneration/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/export-template-as-html.md) for the provider-specific parameters and requirements.

