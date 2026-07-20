# Explodely: Create Affiliate Referral Contract

Creates a new affiliate referral contract in Explodely.

```
POST https://connect.mindcloud.co/v1/universal/explodely/latest/actions/create-affiliate-referral-contract
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Explodely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/explodely/latest/actions/create-affiliate-referral-contract" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contractName": "Sandbox Referral Contract",
  "partnerUsername": "affiliate_username",
  "product": "allproducts",
  "commission": "20"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/explodely/latest/actions/create-affiliate-referral-contract', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contractName": "Sandbox Referral Contract",
    "partnerUsername": "affiliate_username",
    "product": "allproducts",
    "commission": "20"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contractName` | string | yes | A name for the contract in your seller records. Example: `Sandbox Referral Contract`. |
| `partnerUsername` | string | yes | The Explodely affiliate ID of the partner. Example: `affiliate_username`. |
| `product` | string | yes | The Explodely product ID or allproducts. Example: `allproducts`. |
| `commission` | string | yes | The percentage of your share the partner will get, up to 80. Example: `20`. |
| `startDate` | string | no | Optional start date in dd-mmm-yyyy format. Example: `01-jan-2026`. |
| `endDate` | string | no | Optional end date in dd-mmm-yyyy format. Example: `31-jan-2026`. |
| `maxEarnings` | string | no | Optional contract earnings cap. Example: `500`. |
| `maxSales` | string | no | Optional contract sales cap. Example: `10`. |
| `comments` | string | no | Optional comments shown in the seller contracts section. Example: `Optional seller notes`. |
| `activate` | string | no | Set to yes to activate the contract immediately. Example: `yes`. |
| `mutualTermination` | string | no | Set to yes to require both parties to approve termination. Example: `yes`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contract_created": "string",
      "contractid": 1,
      "error": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contract_created` | string |  |
| `contractid` | number |  |
| `error` | string |  |

## Native endpoint

Through the native Explodely API, this operation is `POST /aff` (base URL `https://explodely.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-affiliate-referral-contract.md) for the provider-specific parameters and requirements.

