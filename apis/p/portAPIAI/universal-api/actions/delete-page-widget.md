# Port API AI: Delete Page Widget



```
DELETE https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/delete-page-widget
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Port API AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/delete-page-widget?connectionId=$CONNECTION_ID&pageIdentifier=string&widgetId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "pageIdentifier": "string",
  "widgetId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/delete-page-widget?${params}`, {
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
| `pageIdentifier` | string | yes | The page identifier. |
| `widgetId` | string | yes | The widget identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ok": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ok` | boolean |  |

## Native endpoint

Through the native Port API AI API, this operation is `DELETE /pages/:page_identifier/widgets/:widget_id` (base URL `https://api.port.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-page-widget.md) for the provider-specific parameters and requirements.

