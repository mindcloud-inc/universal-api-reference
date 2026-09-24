# ADP: Create Payroll Batch



```
POST https://connect.mindcloud.co/v1/universal/adp/latest/actions/create-payroll-batch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ADP `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/adp/latest/actions/create-payroll-batch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "companyCode": "string",
  "batchID": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/adp/latest/actions/create-payroll-batch', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "companyCode": "string",
    "batchID": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `companyCode` | string | yes |  |
| `entry[].additionalPayCodes[].payCode` | string | no |  |
| `entry[].fileNumber` | string | no |  |
| `batchID` | string | yes |  |
| `entry[].additionalPayCodes[].hours` | number | no |  |
| `entry[].associateOID` | string | no |  |
| `entry[]` | array | no |  |
| `entry[].regularHours` | number | no |  |
| `entry[].overTimeHours` | number | no |  |
| `entry[].ptoHours` | number | no |  |
| `entry[].holidayHours` | number | no |  |
| `entry[].additionalPayCodes[]` | array | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ADP API returns.

## Native endpoint

Through the native ADP API, this operation is `POST events/payroll/v1/pay-data-input.modify` (base URL `https://api.adp.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-payroll-batch.md) for the provider-specific parameters and requirements.

