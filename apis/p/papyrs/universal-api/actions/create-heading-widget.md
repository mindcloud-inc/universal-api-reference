# Papyrs: Create Heading Widget



```
POST https://connect.mindcloud.co/v1/universal/papyrs/latest/actions/create-heading-widget
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Papyrs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/papyrs/latest/actions/create-heading-widget" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "pageId": "string",
  "widget.val": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/papyrs/latest/actions/create-heading-widget', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "pageId": "string",
    "widget.val": "string"
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
| `widget.val` | string | yes | The text or HTML value for the widget. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "classname": "Ava Chen",
      "html": "string",
      "id": "string",
      "text": "string"
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
| `id` | string | Papyrs widget ID. |
| `text` | string | Plain-text widget content. |

## Native endpoint

Through the native Papyrs API, this operation is `POST /page/:page_id/heading/create/` (base URL `https://{{credentials.subdomain}}.papyrs.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-heading-widget.md) for the provider-specific parameters and requirements.

