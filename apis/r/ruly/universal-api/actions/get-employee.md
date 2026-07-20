# Ruly: Get Employee



```
GET https://connect.mindcloud.co/v1/universal/ruly/latest/actions/get-employee
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ruly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ruly/latest/actions/get-employee?connectionId=$CONNECTION_ID&employeeId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "employeeId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ruly/latest/actions/get-employee?${params}`, {
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
| `employeeId` | string | yes | Employee record identifier from the path. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Ruly API returns.

## Native endpoint

Through the native Ruly API, this operation is `GET data/employee/:employeeId` (base URL `https://mindcloud.api.rulyapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-employee.md) for the provider-specific parameters and requirements.

