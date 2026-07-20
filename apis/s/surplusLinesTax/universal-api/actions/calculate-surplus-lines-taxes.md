# Surplus Lines Tax: Calculate Surplus Lines Taxes



```
POST https://connect.mindcloud.co/v1/universal/surplusLinesTax/latest/actions/calculate-surplus-lines-taxes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Surplus Lines Tax `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/surplusLinesTax/latest/actions/calculate-surplus-lines-taxes" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "state": "string",
  "premium": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/surplusLinesTax/latest/actions/calculate-surplus-lines-taxes', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "state": "string",
    "premium": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `state` | string | yes | State name or two-letter abbreviation. |
| `premium` | number | yes | Premium amount in USD. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `effectiveDate` | date | no | Historical calculation date in YYYY-MM-DD format. |
| `year` | number | no | Tax year used for Iowa's phased-down rates. |
| `wetMarine` | boolean | no | Use Alaska's wet marine tax treatment. |
| `fireInsurance` | boolean | no | Apply fire insurance rules where supported. |
| `electronicFiling` | boolean | no | Apply electronic filing rules where supported. |
| `fireMarshalRate` | number | no | Fire marshal tax rate as a decimal between 0 and 0.01 for Illinois. |
| `medicalMalpractice` | boolean | no | Apply Puerto Rico medical malpractice exemption. |
| `workersComp` | boolean | no | Apply Virginia workers compensation exemption. |
| `newBusiness` | boolean | no | Include Oregon's new or renewal policy service charge. Default: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account": {
        "balance": "string",
        "freeQueriesRemaining": 1,
        "wasFreeQuery": true
      },
      "breakdown": {
        "baseTax": {
          "amount": 1,
          "rate": "string"
        },
        "fireMarshalTax": {
          "amount": 1,
          "rate": "string"
        },
        "flatFee": {
          "amount": 1,
          "rate": "string"
        },
        "stampingFee": {
          "amount": 1,
          "rate": "string"
        }
      },
      "legislativeSource": "string",
      "notes": [
        "string"
      ],
      "premium": 1,
      "ratesFrom": "string",
      "state": "string",
      "stateCode": "string",
      "success": true,
      "totalDue": 1,
      "totalTax": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account.balance` | string |  |
| `account.freeQueriesRemaining` | number |  |
| `account.wasFreeQuery` | boolean |  |
| `breakdown.baseTax.amount` | number |  |
| `breakdown.baseTax.rate` | string |  |
| `breakdown.fireMarshalTax.amount` | number |  |
| `breakdown.fireMarshalTax.rate` | string |  |
| `breakdown.flatFee.amount` | number |  |
| `breakdown.flatFee.rate` | string |  |
| `breakdown.stampingFee.amount` | number |  |
| `breakdown.stampingFee.rate` | string |  |
| `legislativeSource` | string |  |
| `notes[]` | string |  |
| `premium` | number |  |
| `ratesFrom` | string |  |
| `state` | string |  |
| `stateCode` | string |  |
| `success` | boolean |  |
| `totalDue` | number |  |
| `totalTax` | number |  |

## Native endpoint

Through the native Surplus Lines Tax API, this operation is `POST /calculate` (base URL `https://api.surpluslinesapi.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/calculate-surplus-lines-taxes.md) for the provider-specific parameters and requirements.

