# Favro: Get Widget

Retrieves a widget from Favro by widget ID.

```
GET https://connect.mindcloud.co/v1/universal/favro/latest/actions/get-widget
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Favro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/favro/latest/actions/get-widget?connectionId=$CONNECTION_ID&widgetCommonId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "widgetCommonId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/favro/latest/actions/get-widget?${params}`, {
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
| `widgetCommonId` | string | yes | The Favro widget common ID to retrieve. |

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

Through the native Favro API, this operation is `GET /widgets/:widgetCommonId` (base URL `https://favro.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-widget.md) for the provider-specific parameters and requirements.

