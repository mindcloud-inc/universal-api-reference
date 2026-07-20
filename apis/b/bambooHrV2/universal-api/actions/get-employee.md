# BambooHR: Get Employee

Retrieves details for one employee from BambooHR.

```
GET https://connect.mindcloud.co/v1/universal/bambooHrV2/latest/actions/get-employee
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BambooHR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bambooHrV2/latest/actions/get-employee?connectionId=$CONNECTION_ID&employeeId=4" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "employeeId": "4"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bambooHrV2/latest/actions/get-employee?${params}`, {
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
| `employeeId` | string | yes | The BambooHR employee identifier to retrieve from the employee path segment. Example: `4`. |
| `fields` | string | no | Optional comma-separated BambooHR field IDs to return. Defaults to a useful employee summary set when left blank. Default: `firstName,lastName,jobTitle,status`. Example: `firstName,lastName,jobTitle`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native BambooHR API returns.

## Native endpoint

Through the native BambooHR API, this operation is `GET /v1/employees/:id` (base URL `https://mindcloud.bamboohr.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-employee.md) for the provider-specific parameters and requirements.

