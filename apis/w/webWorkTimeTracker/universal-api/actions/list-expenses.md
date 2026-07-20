# WebWork Time Tracker: List Expenses

Retrieves expenses from WebWork Time Tracker.

```
GET https://connect.mindcloud.co/v1/universal/webWorkTimeTracker/latest/actions/list-expenses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WebWork Time Tracker `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webWorkTimeTracker/latest/actions/list-expenses?connectionId=$CONNECTION_ID&limit=25&offset=0&workspaceId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "workspaceId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webWorkTimeTracker/latest/actions/list-expenses?${params}`, {
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
| `workspaceId` | number | yes | ID of the workspace. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addedDte": "string",
      "amount": 1,
      "category": "string",
      "expenseDate": "string",
      "expenseName": "Ava Chen",
      "id": "string",
      "member": "string",
      "note": {},
      "project": {},
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addedDte` | string |  |
| `amount` | number |  |
| `category` | string |  |
| `expenseDate` | string |  |
| `expenseName` | string |  |
| `id` | string |  |
| `member` | string |  |
| `note` | object |  |
| `project` | object |  |
| `type` | string |  |

## Native endpoint

Through the native WebWork Time Tracker API, this operation is `GET /expenses` (base URL `https://api.webwork-tracker.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-expenses.md) for the provider-specific parameters and requirements.

