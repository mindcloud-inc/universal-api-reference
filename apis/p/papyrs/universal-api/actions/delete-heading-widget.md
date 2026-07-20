# Papyrs: Delete Heading Widget



```
DELETE https://connect.mindcloud.co/v1/universal/papyrs/latest/actions/delete-heading-widget
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Papyrs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/papyrs/latest/actions/delete-heading-widget?connectionId=$CONNECTION_ID&pageId=string&widgetId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "pageId": "string",
  "widgetId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/papyrs/latest/actions/delete-heading-widget?${params}`, {
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
      "deleted": true,
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deleted` | boolean | Whether the widget was deleted. |
| `id` | string | Deleted Papyrs widget ID. |

## Native endpoint

Through the native Papyrs API, this operation is `POST /page/:page_id/heading/delete/:widget_id/` (base URL `https://{{credentials.subdomain}}.papyrs.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-heading-widget.md) for the provider-specific parameters and requirements.

