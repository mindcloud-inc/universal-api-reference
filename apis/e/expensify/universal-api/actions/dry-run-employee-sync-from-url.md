# Expensify: Dry Run Employee Sync From URL

Retrieves a dry-run employee sync from a URL in Expensify.

```
GET https://connect.mindcloud.co/v1/universal/expensify/latest/actions/dry-run-employee-sync-from-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Expensify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/expensify/latest/actions/dry-run-employee-sync-from-url?connectionId=$CONNECTION_ID&feedUrl=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "feedUrl": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/expensify/latest/actions/dry-run-employee-sync-from-url?${params}`, {
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
| `feedUrl` | string | yes | HTTPS URL that Expensify should download the employee JSON feed from. |
| `feedUser` | string | no | Optional Basic Auth username for the employee feed URL. |
| `feedPassword` | string | no | Optional Basic Auth password for the employee feed URL. |

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

Through the native Expensify API, this operation is `POST ExpensifyIntegrations` (base URL `https://integrations.expensify.com/Integration-Server/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/dry-run-employee-sync-from-url.md) for the provider-specific parameters and requirements.

