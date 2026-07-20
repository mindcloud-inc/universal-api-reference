# BambooHR: Get Changed Employees

Retrieves changed employee IDs from BambooHR.

```
GET https://connect.mindcloud.co/v1/universal/bambooHrV2/latest/actions/get-changed-employees
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BambooHR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bambooHrV2/latest/actions/get-changed-employees?connectionId=$CONNECTION_ID&since=2026-03-01T00%3A00%3A00Z" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "since": "2026-03-01T00:00:00Z"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bambooHrV2/latest/actions/get-changed-employees?${params}`, {
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
| `since` | string | yes | Return employees changed after this ISO-8601 timestamp. Example: `2026-03-01T00:00:00Z`. |
| `changeType` | string | no | Optional change type filter. Use inserted, updated, or deleted. Example: `updated`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native BambooHR API returns.

## Native endpoint

Through the native BambooHR API, this operation is `GET /v1/employees/changed/[:type]` (base URL `https://mindcloud.bamboohr.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-changed-employees.md) for the provider-specific parameters and requirements.

