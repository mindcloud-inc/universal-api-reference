# Ruly: Update Employee City



```
PUT https://connect.mindcloud.co/v1/universal/ruly/latest/actions/update-employee-city
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ruly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/ruly/latest/actions/update-employee-city" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "city": "string",
  "employeeId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ruly/latest/actions/update-employee-city', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "city": "string",
    "employeeId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `city` | string | yes | Employee city value to update. |
| `employeeId` | string | yes | Employee record identifier from the path. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Ruly API returns.

## Native endpoint

Through the native Ruly API, this operation is `PUT data/employee/:employeeId` (base URL `https://mindcloud.api.rulyapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-employee-city.md) for the provider-specific parameters and requirements.

