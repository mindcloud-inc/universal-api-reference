# Favro: Delete Widget

Deletes an existing widget from Favro.

```
DELETE https://connect.mindcloud.co/v1/universal/favro/latest/actions/delete-widget
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Favro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/favro/latest/actions/delete-widget?connectionId=$CONNECTION_ID&widgetCommonId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "widgetCommonId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/favro/latest/actions/delete-widget?${params}`, {
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
| `collectionId` | string | no | Delete the widget from one collection only when provided. |
| `widgetCommonId` | string | yes | The widget common ID to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "widgetCommonId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `widgetCommonId` | string |  |

## Native endpoint

Through the native Favro API, this operation is `DELETE /widgets/:widgetCommonId` (base URL `https://favro.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-widget.md) for the provider-specific parameters and requirements.

