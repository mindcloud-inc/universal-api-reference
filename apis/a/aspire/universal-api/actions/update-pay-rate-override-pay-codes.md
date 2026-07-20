# Aspire: Update Pay Rate Override Pay Codes

Updates an existing pay rate override pay code in your Aspire account.

```
PUT https://connect.mindcloud.co/v1/universal/aspire/latest/actions/update-pay-rate-override-pay-codes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspire `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/aspire/latest/actions/update-pay-rate-override-pay-codes" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "payRateId": 1,
  "payCodeId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/aspire/latest/actions/update-pay-rate-override-pay-codes', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "payRateId": 1,
    "payCodeId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `payRateId` | list<number> | yes |  |
| `payCodeId` | list | yes |  |
| `overrideRate` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "burdenPercent": 1,
      "contactID": 1,
      "contactName": "Ava Chen",
      "effectiveDate": "string",
      "hourlyBasePay": 1,
      "payRateID": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `burdenPercent` | number |  |
| `contactID` | number |  |
| `contactName` | string |  |
| `effectiveDate` | string |  |
| `hourlyBasePay` | number |  |
| `payRateID` | number |  |

## Native endpoint

Through the native Aspire API, this operation is `PUT PayRateOverridePayCodes` (base URL `https://{{credentials.environment}}.youraspire.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/update-pay-rate-override-pay-codes.md) for the provider-specific parameters and requirements.

