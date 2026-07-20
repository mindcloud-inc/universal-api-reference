# Laposta: Create List

Creates a new list in Laposta.

```
POST https://connect.mindcloud.co/v1/universal/laposta/latest/actions/create-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Laposta `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/laposta/latest/actions/create-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/laposta/latest/actions/create-list', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Name of the list to create. |
| `locked` | boolean | no | Whether the list is locked from user edits. |
| `remarks` | string | no | Optional remarks for the list. |
| `subscribeNotificationEmail` | string | no | Email address notified on new subscriptions. |
| `unsubscribeNotificationEmail` | string | no | Email address notified on unsubscribes. |

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

Through the native Laposta API, this operation is `POST /list` (base URL `https://api.laposta.nl/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-list.md) for the provider-specific parameters and requirements.

