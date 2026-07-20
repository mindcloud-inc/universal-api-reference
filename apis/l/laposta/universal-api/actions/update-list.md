# Laposta: Update List

Updates an existing list in Laposta.

```
PUT https://connect.mindcloud.co/v1/universal/laposta/latest/actions/update-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Laposta `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/laposta/latest/actions/update-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "listId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/laposta/latest/actions/update-list', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "listId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `listId` | string | yes | The ID of the list to update. |
| `name` | string | no | Updated list name. |
| `locked` | boolean | no | Whether the list is locked. |
| `remarks` | string | no | Updated list remarks. |
| `subscribeNotificationEmail` | string | no | Notification email for subscriptions. |
| `unsubscribeNotificationEmail` | string | no | Notification email for unsubscriptions. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "list": {
        "listId": "string",
        "locked": true,
        "name": "Ava Chen",
        "remarks": "string",
        "state": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `list` | object |  |
| `list.listId` | string |  |
| `list.locked` | boolean |  |
| `list.name` | string |  |
| `list.remarks` | string |  |
| `list.state` | string |  |

## Native endpoint

Through the native Laposta API, this operation is `POST /list/:listId` (base URL `https://api.laposta.nl/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-list.md) for the provider-specific parameters and requirements.

