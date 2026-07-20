# Favro: Update Widget

Updates an existing widget in Favro.

```
PUT https://connect.mindcloud.co/v1/universal/favro/latest/actions/update-widget
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Favro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/favro/latest/actions/update-widget" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "widgetCommonId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/favro/latest/actions/update-widget', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "widgetCommonId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `color` | string | no | The widget color. |
| `name` | string | no | The new widget name. |
| `widgetCommonId` | string | yes | The widget common ID to update. |

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

Through the native Favro API, this operation is `PUT /widgets/:widgetCommonId` (base URL `https://favro.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-widget.md) for the provider-specific parameters and requirements.

