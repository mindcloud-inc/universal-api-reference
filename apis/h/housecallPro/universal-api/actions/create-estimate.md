# Housecall Pro: Create Estimate



```
POST https://connect.mindcloud.co/v1/universal/housecallPro/latest/actions/create-estimate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Housecall Pro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/housecallPro/latest/actions/create-estimate" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "options[]": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/housecallPro/latest/actions/create-estimate', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "options[]": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerId` | string | no | Example: `cus_ccdcb54ddb5a42bea9466d386a637af8`. |
| `addressId` | string | no | Example: `adr_fe965ac68e864b408c41b420abcfd902`. |
| `note` | string | no | Example: `Estimate created during stage 3 buildout.`. |
| `message` | string | no | Example: `Thanks for reviewing this estimate.`. |
| `options[]` | array<object> | yes | Example: `[object Object]`. |
| `options[].name` | string | no | Example: `Base Option`. |
| `options[].tags[]` | array<string> | no | Accepts multiple values as an array. Example: `standard`. |
| `options[].lineItems[]` | array<object> | no | Example: `[object Object]`. |
| `schedule` | object | no | Example: `[object Object]`. |
| `schedule.startTime` | date | no | Example: `2026-03-11T15:00:00Z`. |
| `schedule.endTime` | date | no | Example: `2026-03-11T16:00:00Z`. |
| `schedule.arrivalWindowInMinutes` | number | no | Example: `30`. |
| `schedule.notifyCustomer` | boolean | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `assignedEmployeeIds[]` | array<string> | no | Accepts multiple values as an array. |
| `leadSource` | string | no | Example: `web`. |
| `address` | object | no | Example: `[object Object]`. |
| `address.street` | string | no | Example: `701 S Harrison Ave`. |
| `address.streetLine2` | string | no | Example: `Suite 200`. |
| `address.city` | string | no | Example: `Kankakee`. |
| `address.state` | string | no | Example: `IL`. |
| `address.zip` | string | no | Example: `60901`. |
| `tax` | object | no | Example: `[object Object]`. |
| `tax.taxable` | boolean | no |  |
| `tax.taxRate` | number | no | Example: `8.25`. |
| `tax.taxName` | string | no | Example: `Sales Tax`. |
| `estimateFields` | object | no | Example: `[object Object]`. |
| `estimateFields.jobTypeId` | string | no | Example: `jobtype_123`. |
| `estimateFields.businessUnitId` | string | no | Example: `bu_123`. |
| `estimateNumber` | number | no | Estimate number unique across all company estimates. If left blank, one will be generated automatically. Example: `1001`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": {},
      "assignedEmployees": [
        {}
      ],
      "companyId": "string",
      "companyName": "Ava Chen",
      "createdAt": "string",
      "customer": {},
      "estimateFields": {},
      "estimateNumber": "string",
      "id": "string",
      "leadSource": "string",
      "options": [
        {}
      ],
      "schedule": {},
      "updatedAt": "string",
      "workStatus": "string",
      "workTimestamps": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | object |  |
| `assignedEmployees` | array<object> |  |
| `companyId` | string |  |
| `companyName` | string |  |
| `createdAt` | string |  |
| `customer` | object |  |
| `estimateFields` | object |  |
| `estimateNumber` | string |  |
| `id` | string |  |
| `leadSource` | string |  |
| `options` | array<object> |  |
| `schedule` | object |  |
| `updatedAt` | string |  |
| `workStatus` | string |  |
| `workTimestamps` | object |  |

## Native endpoint

Through the native Housecall Pro API, this operation is `POST /estimates` (base URL `https://api.housecallpro.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-estimate.md) for the provider-specific parameters and requirements.

