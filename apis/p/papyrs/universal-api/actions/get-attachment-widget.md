# Papyrs: Get Attachment Widget



```
GET https://connect.mindcloud.co/v1/universal/papyrs/latest/actions/get-attachment-widget
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Papyrs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/papyrs/latest/actions/get-attachment-widget?connectionId=$CONNECTION_ID&pageId=string&widgetId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "pageId": "string",
  "widgetId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/papyrs/latest/actions/get-attachment-widget?${params}`, {
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

Through the native Papyrs API, this operation is `GET /page/:page_id/attachment/get/:widget_id/` (base URL `https://{{credentials.subdomain}}.papyrs.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-attachment-widget.md) for the provider-specific parameters and requirements.

