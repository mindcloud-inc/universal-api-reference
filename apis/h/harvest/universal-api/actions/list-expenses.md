# Harvest: List Expenses

Retrieves expenses from Harvest.

```
GET https://connect.mindcloud.co/v1/universal/harvest/latest/actions/list-expenses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Harvest `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/harvest/latest/actions/list-expenses?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/harvest/latest/actions/list-expenses?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "approvalStatus": "string",
      "billable": true,
      "client": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "expenseCategory": {},
      "id": 1,
      "invoice": {},
      "isBilled": true,
      "isClosed": true,
      "isLocked": true,
      "lockedReason": "string",
      "notes": "string",
      "project": {},
      "receipt": {},
      "spentDate": "2026-05-07T12:00:00.000Z",
      "totalCost": 1,
      "units": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "user": {},
      "userAssignment": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `approvalStatus` | string |  |
| `billable` | boolean |  |
| `client` | object |  |
| `createdAt` | date |  |
| `expenseCategory` | object |  |
| `id` | number |  |
| `invoice` | object |  |
| `isBilled` | boolean |  |
| `isClosed` | boolean |  |
| `isLocked` | boolean |  |
| `lockedReason` | string |  |
| `notes` | string |  |
| `project` | object |  |
| `receipt` | object |  |
| `spentDate` | date |  |
| `totalCost` | number |  |
| `units` | number |  |
| `updatedAt` | date |  |
| `user` | object |  |
| `userAssignment` | object |  |

## Native endpoint

Through the native Harvest API, this operation is `GET /v2/expenses` (base URL `https://api.harvestapp.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-expenses.md) for the provider-specific parameters and requirements.

