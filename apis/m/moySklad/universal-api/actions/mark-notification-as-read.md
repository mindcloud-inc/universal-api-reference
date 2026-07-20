# MoySklad: Mark notification as read

Marks a notification as read in MoySklad.

```
PUT https://connect.mindcloud.co/v1/universal/moySklad/latest/actions/mark-notification-as-read
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MoySklad `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/moySklad/latest/actions/mark-notification-as-read" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moySklad/latest/actions/mark-notification-as-read', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | MoySklad notification ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "meta": {},
      "read": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `meta` | object |  |
| `read` | boolean |  |

## Native endpoint

Through the native MoySklad API, this operation is `PUT notification/:id/markasread` (base URL `https://api.moysklad.ru/api/remap/1.2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/mark-notification-as-read.md) for the provider-specific parameters and requirements.

