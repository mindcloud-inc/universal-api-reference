# SmartrMail: Update Subscriber List

Updates an existing subscriber list in SmartrMail.

```
PUT https://connect.mindcloud.co/v1/universal/smartrMail/latest/actions/update-subscriber-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SmartrMail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/smartrMail/latest/actions/update-subscriber-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "listId": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/smartrMail/latest/actions/update-subscriber-list', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "listId": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `listId` | string | yes | The ID of the requested list. |
| `name` | string | yes | The updated name of the subscriber list. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen",
      "subscribers_count": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `name` | string |  |
| `subscribers_count` | number |  |

## Native endpoint

Through the native SmartrMail API, this operation is `PUT /lists/:list_id` (base URL `https://go.smartrmail.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-subscriber-list.md) for the provider-specific parameters and requirements.

