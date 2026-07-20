# BoardCRM: Change Deal Column

Moves deals between columns in BoardCRM.

```
PUT https://connect.mindcloud.co/v1/universal/boardCRM/latest/actions/change-deal-column
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BoardCRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/boardCRM/latest/actions/change-deal-column" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "columnIdFrom": 1,
  "columnIdTo": 1,
  "ids[]": [
    1
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/boardCRM/latest/actions/change-deal-column', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "columnIdFrom": 1,
    "columnIdTo": 1,
    "ids[]": [1]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `columnIdFrom` | number | yes | Current deal column ID. |
| `columnIdTo` | number | yes | Destination deal column ID. |
| `ids[]` | array<number> | yes | Deal IDs to move to the destination column. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | number |  |

## Native endpoint

Through the native BoardCRM API, this operation is `POST /offer/change-column` (base URL `https://api.boardcrm.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/change-deal-column.md) for the provider-specific parameters and requirements.

