# Lunch Money: Update an existing category or category group



```
PUT https://connect.mindcloud.co/v1/universal/lunchMoney/latest/actions/update-category
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lunch Money `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/lunchMoney/latest/actions/update-category" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lunchMoney/latest/actions/update-category', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes |  |
| `name` | string | no |  |
| `description` | string | no |  |
| `archived` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "archivedAt": "string",
      "collapsed": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "excludeFromBudget": true,
      "excludeFromTotals": true,
      "groupId": 1,
      "id": 1,
      "isGroup": true,
      "isIncome": true,
      "name": "Ava Chen",
      "order": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `archivedAt` | string |  |
| `collapsed` | boolean |  |
| `createdAt` | date |  |
| `description` | string |  |
| `excludeFromBudget` | boolean |  |
| `excludeFromTotals` | boolean |  |
| `groupId` | number |  |
| `id` | number |  |
| `isGroup` | boolean |  |
| `isIncome` | boolean |  |
| `name` | string |  |
| `order` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Lunch Money API, this operation is `PUT /categories/:id` (base URL `https://api.lunchmoney.dev/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-category.md) for the provider-specific parameters and requirements.

