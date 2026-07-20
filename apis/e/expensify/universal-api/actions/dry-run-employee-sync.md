# Expensify: Dry Run Employee Sync

Retrieves a dry-run employee sync result from Expensify.

```
GET https://connect.mindcloud.co/v1/universal/expensify/latest/actions/dry-run-employee-sync
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Expensify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/expensify/latest/actions/dry-run-employee-sync?connectionId=$CONNECTION_ID&employeesJson=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "employeesJson": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/expensify/latest/actions/dry-run-employee-sync?${params}`, {
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
| `employeesJson` | string | yes | JSON array of employee objects for the Advanced Employee Updater request-mode feed. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dry-run": true,
      "email": "ava@example.com",
      "reason": "string",
      "requestID": "string",
      "responseCode": 1,
      "updatedEmployeesCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dry-run` | boolean |  |
| `email` | string |  |
| `reason` | string |  |
| `requestID` | string |  |
| `responseCode` | number |  |
| `updatedEmployeesCount` | number |  |

## Native endpoint

Through the native Expensify API, this operation is `POST ExpensifyIntegrations` (base URL `https://integrations.expensify.com/Integration-Server/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/dry-run-employee-sync.md) for the provider-specific parameters and requirements.

