# Papyrs: Update Attachment Widget



```
PUT https://connect.mindcloud.co/v1/universal/papyrs/latest/actions/update-attachment-widget
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Papyrs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/papyrs/latest/actions/update-attachment-widget" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string",
  "pageId": "string",
  "widgetId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/papyrs/latest/actions/update-attachment-widget', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "string",
    "pageId": "string",
    "widgetId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file` | file | yes | The file to add to the existing attachment widget. |
| `pageId` | string | yes | The Papyrs page ID. |
| `widgetId` | string | yes | The Papyrs widget ID on the page. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "classname": "Ava Chen",
      "files": [
        {
          "filename": "Ava Chen",
          "size": 1,
          "url": "https://example.com",
          "vanity_size": "string"
        }
      ],
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `classname` | string | Widget class name. |
| `files` | array<object> | Files attached to the widget. |
| `files[].filename` | string | Uploaded file name. |
| `files[].size` | number | Uploaded file size in bytes. |
| `files[].url` | string | Absolute file URL. |
| `files[].vanity_size` | string | Human-readable file size. |
| `id` | string | Papyrs widget ID. |

## Native endpoint

Through the native Papyrs API, this operation is `POST /page/:page_id/attachment/update/:widget_id/` (base URL `https://{{credentials.subdomain}}.papyrs.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-attachment-widget.md) for the provider-specific parameters and requirements.

