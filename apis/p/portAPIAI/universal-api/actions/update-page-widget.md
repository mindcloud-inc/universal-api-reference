# Port API AI: Update Page Widget



```
PUT https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/update-page-widget
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Port API AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/update-page-widget" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "blueprint": "string",
  "blueprintConfig": {},
  "dataset": {},
  "pageIdentifier": "string",
  "type": "string",
  "widgetId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/update-page-widget', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "blueprint": "string",
    "blueprintConfig": {},
    "dataset": {},
    "pageIdentifier": "string",
    "type": "string",
    "widgetId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `blueprint` | string | yes | Blueprint identifier |
| `blueprintConfig` | object | yes | Widget blueprint config |
| `dataset` | object | yes | Widget dataset |
| `pageIdentifier` | string | yes | The page identifier. |
| `type` | string | yes | Widget type |
| `widgetId` | string | yes | The widget identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "identifier": "string",
      "ok": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `identifier` | string |  |
| `ok` | boolean |  |

## Native endpoint

Through the native Port API AI API, this operation is `PATCH /pages/:page_identifier/widgets/:widget_id` (base URL `https://api.port.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-page-widget.md) for the provider-specific parameters and requirements.

