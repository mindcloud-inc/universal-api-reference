# NetSuite - Advanced: Update Employee



```
PUT https://connect.mindcloud.co/v1/universal/netsuite/latest/actions/update-employee
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetSuite - Advanced `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/netsuite/latest/actions/update-employee" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/netsuite/latest/actions/update-employee', {
  method: 'PUT',
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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `recordId` | list<number> | no |  |
| `columns` | object | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native NetSuite - Advanced API returns.

## Native endpoint

Through the native NetSuite - Advanced API, this operation is `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` (base URL `https://{{credentials.accountId}}.suitetalk.api.netsuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-employee.md) for the provider-specific parameters and requirements.

