# Paymo: List Tasks

Retrieves tasks from Paymo.

```
GET https://connect.mindcloud.co/v1/universal/paymo/latest/actions/list-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paymo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/paymo/latest/actions/list-tasks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/paymo/latest/actions/list-tasks?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `where` | string | no | Optional raw Paymo filtering expression, for example `tasklist_id=7096346`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "billable": true,
      "billingType": "string",
      "code": "string",
      "complete": true,
      "createdOn": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "flatBilling": true,
      "id": 1,
      "name": "Ava Chen",
      "priority": 1,
      "projectId": 1,
      "statusId": 1,
      "tasklistId": 1,
      "updatedOn": "2026-05-07T12:00:00.000Z",
      "userId": 1,
      "users": [
        1
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billable` | boolean |  |
| `billingType` | string |  |
| `code` | string |  |
| `complete` | boolean |  |
| `createdOn` | date |  |
| `description` | string |  |
| `flatBilling` | boolean |  |
| `id` | number |  |
| `name` | string |  |
| `priority` | number |  |
| `projectId` | number |  |
| `statusId` | number |  |
| `tasklistId` | number |  |
| `updatedOn` | date |  |
| `userId` | number |  |
| `users` | array<number> |  |

## Native endpoint

Through the native Paymo API, this operation is `GET tasks` (base URL `https://app.paymoapp.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-tasks.md) for the provider-specific parameters and requirements.

