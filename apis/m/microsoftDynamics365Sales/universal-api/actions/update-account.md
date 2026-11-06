# Microsoft Dynamics 365 Sales: Update Account



```
PUT https://connect.mindcloud.co/v1/universal/microsoftDynamics365Sales/latest/actions/update-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Dynamics 365 Sales `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/microsoftDynamics365Sales/latest/actions/update-account" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": "00000000-0000-0000-0000-000000000001"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoftDynamics365Sales/latest/actions/update-account', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": "00000000-0000-0000-0000-000000000001"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | string | yes | Example: `00000000-0000-0000-0000-000000000001`. |
| `fields` | object | no | Map an object containing only the columns to change, or fill the individual fields below. Use native column logical names for custom fields. |
| `fields.name` | string | no |  |
| `fields.accountNumber` | string | no |  |
| `fields.description` | string | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fields.emailAddress1` | string | no |  |
| `fields.telephone1` | string | no |  |
| `fields.telephone2` | string | no |  |
| `fields.websiteUrl` | string | no |  |
| `fields.revenue` | number | no |  |
| `fields.numberOfEmployees` | number | no |  |
| `fields.creditLimit` | number | no |  |
| `fields.creditOnHold` | boolean | no |  |
| `fields.doNotEmail` | boolean | no |  |
| `fields.doNotPhone` | boolean | no |  |
| `fields.address1Line1` | string | no |  |
| `fields.address1Line2` | string | no |  |
| `fields.address1City` | string | no |  |
| `fields.address1StateOrProvince` | string | no |  |
| `fields.address1PostalCode` | string | no |  |
| `fields.address1Country` | string | no |  |
| `select` | string | no | Comma-separated column logical names to return. Accepts multiple values in one string, delimited by `,`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Microsoft Dynamics 365 Sales API returns.

## Native endpoint

Through the native Microsoft Dynamics 365 Sales API, this operation is `PATCH /accounts(:accountId)` (base URL `{{credentials.environmentUrl}}/api/data/v9.2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-account.md) for the provider-specific parameters and requirements.

