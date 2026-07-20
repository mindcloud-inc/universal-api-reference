# Aspire: Create Pay Rate Override Pay Codes

Creates a new pay rate override pay code in your Aspire account.

```
POST https://connect.mindcloud.co/v1/universal/aspire/latest/actions/create-pay-rate-override-pay-codes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspire `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/aspire/latest/actions/create-pay-rate-override-pay-codes" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/aspire/latest/actions/create-pay-rate-override-pay-codes', {
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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `payRateId` | list<number> | no |  |
| `payCodeId` | list<number> | no |  |
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

Through the native Aspire API, this operation is `POST PayRateOverridePayCodes` (base URL `https://{{credentials.environment}}.youraspire.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/create-pay-rate-override-pay-codes.md) for the provider-specific parameters and requirements.

