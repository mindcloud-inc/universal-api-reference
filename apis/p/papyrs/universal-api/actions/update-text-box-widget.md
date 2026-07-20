# Papyrs: Update Text Box Widget



```
PUT https://connect.mindcloud.co/v1/universal/papyrs/latest/actions/update-text-box-widget
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Papyrs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/papyrs/latest/actions/update-text-box-widget" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "pageId": "string",
  "widget.val": "string",
  "widgetId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/papyrs/latest/actions/update-text-box-widget', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "pageId": "string",
    "widget.val": "string",
    "widgetId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `format` | string | no | Optional format for widget.val. Defaults to html. Default: `html`. |
| `pageId` | string | yes | The Papyrs page ID. |
| `widget.val` | string | yes | The updated text or HTML value for the widget. |
| `widgetId` | string | yes | The Papyrs widget ID on the page. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "classname": "Ava Chen",
      "html": "string",
      "id": "string",
      "text": "string",
      "version_of_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `classname` | string | Widget class name. |
| `html` | string | Rendered widget HTML. |
| `id` | string | Current Papyrs widget ID. |
| `text` | string | Plain-text widget content. |
| `version_of_id` | string | Previous widget ID that this version replaces. |

## Native endpoint

Through the native Papyrs API, this operation is `POST /page/:page_id/paragraph/update/:widget_id/` (base URL `https://{{credentials.subdomain}}.papyrs.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-text-box-widget.md) for the provider-specific parameters and requirements.

