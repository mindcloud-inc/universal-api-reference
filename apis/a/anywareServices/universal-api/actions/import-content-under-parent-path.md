# Anyware Services: Import Content Under Parent Path

Creates a page and imported content under a parent path in Anyware Services.

```
POST https://connect.mindcloud.co/v1/universal/anywareServices/latest/actions/import-content-under-parent-path
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Anyware Services `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/anywareServices/latest/actions/import-content-under-parent-path" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "site": "string",
  "lang": "string",
  "path": "string",
  "content": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/anywareServices/latest/actions/import-content-under-parent-path', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "site": "string",
    "lang": "string",
    "path": "string",
    "content": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `site` | string | yes | Target Ametys site name. |
| `lang` | string | yes | Sitemap language where the page and content will be created. |
| `path` | string | yes | Optional parent page path documented by Content IO; use this action when importing below a parent page. |
| `content` | file | yes | XML content file using the Content IO import format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error": "string",
      "errors": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error` | string | Error message returned when the import fails. |
| `errors` | string | Error container returned by the XML ActionResult payload. |
| `success` | boolean | Whether the Content IO import completed successfully. |

## Native endpoint

Through the native Anyware Services API, this operation is `POST /_contentio/import/content/:site/:lang/:path` (base URL `https://demo.ametys.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/import-content-under-parent-path.md) for the provider-specific parameters and requirements.

