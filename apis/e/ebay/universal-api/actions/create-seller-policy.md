# eBay: Create a Selling Policy

Retrieve a specific list of seller policies (i.e. fulfillment, payment & return policies)

```
GET https://connect.mindcloud.co/v1/universal/ebay/latest/actions/create-seller-policy
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eBay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ebay/latest/actions/create-seller-policy?connectionId=$CONNECTION_ID&name=Ava%20Chen&policy=string&marketplaceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "name": "Ava Chen",
  "policy": "string",
  "marketplaceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ebay/latest/actions/create-seller-policy?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | A seller-defined name for this return business policy. Names must be unique for policies assigned to the same marketplace. |
| `policy` | list<string> | yes | Specify which type of policies to create. Accepted values are: payment_policy, return_policy, fulfillment_policy, and custom_policy. |
| `marketplaceId` | string | yes | The eBay marketplace_id to retrieve the specified policies from. |
| `description` | string | no | A seller-defined description of the return business policy. This description is only for the seller's use, and is not exposed on any eBay pages. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "categoryTypes": [
        {
          "name": "Ava Chen"
        }
      ],
      "description": "string",
      "internationalOverride": {
        "returnMethod": "string",
        "returnPeriod": {
          "unit": "string",
          "value": 1
        },
        "returnsAccepted": true,
        "returnShippingCostPayer": "string"
      },
      "marketplaceId": "string",
      "name": "Ava Chen",
      "refundMethod": "string",
      "returnMethod": "string",
      "returnPeriod": {
        "unit": "string",
        "value": 1
      },
      "returnPolicyId": "string",
      "returnsAccepted": true,
      "returnShippingCostPayer": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `categoryTypes[].name` | string |  |
| `description` | string |  |
| `internationalOverride.returnMethod` | string |  |
| `internationalOverride.returnPeriod.unit` | string |  |
| `internationalOverride.returnPeriod.value` | number |  |
| `internationalOverride.returnsAccepted` | boolean |  |
| `internationalOverride.returnShippingCostPayer` | string |  |
| `marketplaceId` | string |  |
| `name` | string |  |
| `refundMethod` | string |  |
| `returnMethod` | string |  |
| `returnPeriod.unit` | string |  |
| `returnPeriod.value` | number |  |
| `returnPolicyId` | string |  |
| `returnsAccepted` | boolean |  |
| `returnShippingCostPayer` | string |  |

## Native endpoint

Through the native eBay API, this operation is `POST sell/account/v1/:policy` (base URL `https://api.ebay.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-seller-policy.md) for the provider-specific parameters and requirements.

