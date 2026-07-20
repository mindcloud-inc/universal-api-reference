# Favro: Create Widget

Creates a new widget in Favro.

```
POST https://connect.mindcloud.co/v1/universal/favro/latest/actions/create-widget
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Favro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/favro/latest/actions/create-widget" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "collectionId": "string",
  "name": "Ava Chen",
  "type": "board"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/favro/latest/actions/create-widget', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "collectionId": "string",
    "name": "Ava Chen",
    "type": "board"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `collectionId` | string | yes | The collection ID where the widget will be created. |
| `name` | string | yes | The name of the widget. |
| `type` | string | yes | The widget type to create. Default: `board`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "collectionIds": [
        "string"
      ],
      "color": "string",
      "columns": [
        {}
      ],
      "editRole": "string",
      "name": "Ava Chen",
      "organizationId": "string",
      "ownerRole": "string",
      "type": "string",
      "widgetCommonId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `collectionIds` | array<string> |  |
| `color` | string |  |
| `columns` | array<object> |  |
| `editRole` | string |  |
| `name` | string |  |
| `organizationId` | string |  |
| `ownerRole` | string |  |
| `type` | string |  |
| `widgetCommonId` | string |  |

## Native endpoint

Through the native Favro API, this operation is `POST /widgets` (base URL `https://favro.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-widget.md) for the provider-specific parameters and requirements.

