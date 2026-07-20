# Stripo: Export Email as HTML

Exports an email as an HTML file from Stripo.

```
GET https://connect.mindcloud.co/v1/universal/stripo/latest/actions/export-email-as-html
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stripo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stripo/latest/actions/export-email-as-html?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stripo/latest/actions/export-email-as-html?${params}`, {
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
| `id` | number | yes | The email ID. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `asAmp` | boolean | no | Return AMPHTML code. |
| `includeTranslationVersions` | boolean | no | Include translated versions in the export. |
| `minimize` | boolean | no | Compress the email output. |
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
| `file` | string | Exported email HTML file content returned by Stripo. |

## Native endpoint

Through the native Stripo API, this operation is `GET /export/html/emails/:id` (base URL `https://my.stripo.email/emailgeneration/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/export-email-as-html.md) for the provider-specific parameters and requirements.

