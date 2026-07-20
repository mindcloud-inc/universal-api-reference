# Weekdone: Assign Item

Assigns an item to a user in Weekdone.

```
PUT https://connect.mindcloud.co/v1/universal/weekdone/latest/actions/assign-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Weekdone `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/weekdone/latest/actions/assign-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "itemId": 1,
  "userId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/weekdone/latest/actions/assign-item', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "itemId": 1,
    "userId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `itemId` | number | yes |  |
| `userId` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string |  |

## Native endpoint

Through the native Weekdone API, this operation is `PATCH item/:itemId/assign` (base URL `https://api.weekdone.com/1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/assign-item.md) for the provider-specific parameters and requirements.

