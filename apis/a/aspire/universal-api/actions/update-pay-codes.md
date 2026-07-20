# Aspire: Update Pay Codes

Updates an existing pay code in your Aspire account.

```
PUT https://connect.mindcloud.co/v1/universal/aspire/latest/actions/update-pay-codes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/aspire/latest/actions/update-pay-codes" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/aspire/latest/actions/update-pay-codes', {
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
| `excludeFromOT` | boolean | no |  |
| `oTPaycode` | boolean | no |  |
| `active` | boolean | no |  |
| `fixedRate` | number | no |  |
| `payCode` | string | no |  |
| `payCodeName` | string | no |  |
| `payCodeType` | string | no |  |
| `premiumDollars` | number | no |  |
| `premiumPercent` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "excludeFromOT": true,
      "fixedRate": {},
      "oTPaycode": true,
      "payCode": "string",
      "payCodeID": 1,
      "payCodeName": "Ava Chen",
      "payCodeType": "string",
      "premiumDollars": {},
      "premiumPercent": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `excludeFromOT` | boolean |  |
| `fixedRate` | object |  |
| `oTPaycode` | boolean |  |
| `payCode` | string |  |
| `payCodeID` | number |  |
| `payCodeName` | string |  |
| `payCodeType` | string |  |
| `premiumDollars` | object |  |
| `premiumPercent` | object |  |

## Native endpoint

Through the native Aspire API, this operation is `PUT PayCodes` (base URL `https://{{credentials.environment}}.youraspire.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-pay-codes.md) for the provider-specific parameters and requirements.

