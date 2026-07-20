# MILKEE: Create Project

Creates a new project in MILKEE.

```
POST https://connect.mindcloud.co/v1/universal/mILKEE/latest/actions/create-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MILKEE `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mILKEE/latest/actions/create-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "companyId": "4640",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mILKEE/latest/actions/create-project', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "companyId": "4640",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `budget` | number | no | Project budget amount. |
| `companyId` | string | yes | The numeric MILKEE company ID used in the request path. Default: `4640`. |
| `customerId` | number | no | Existing customer ID. Mutually exclusive with New Customer Name. |
| `hourlyRate` | number | no | Project hourly rate. |
| `name` | string | yes | Project name. |
| `newCustomerName` | string | no | Create a new customer and assign the project to it. Mutually exclusive with Customer ID. |
| `projectType` | string | no | Project type: byHour, fixedBudget, or fixedPrice. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |

## Native endpoint

Through the native MILKEE API, this operation is `POST /companies/:companyId/projects` (base URL `https://app.milkee.ch/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-project.md) for the provider-specific parameters and requirements.

