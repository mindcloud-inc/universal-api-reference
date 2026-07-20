# NetSuite - Basic: Create Employee

Creates a new employee in NetSuite.

```
POST https://connect.mindcloud.co/v1/universal/netSuiteBasic/latest/actions/create-employee
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetSuite - Basic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/netSuiteBasic/latest/actions/create-employee" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/netSuiteBasic/latest/actions/create-employee', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native NetSuite - Basic API returns.

## Native endpoint

Through the native NetSuite - Basic API, this operation is `POST /record/v1/employee` (base URL `https://{{credentials.accountDomain}}.suitetalk.api.netsuite.com/services/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-employee.md) for the provider-specific parameters and requirements.

