# Walmart: List Price Incentive Items



```
GET https://connect.mindcloud.co/v1/universal/walmart/latest/actions/list-price-incentive-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Walmart `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/walmart/latest/actions/list-price-incentive-items?connectionId=$CONNECTION_ID&incentiveStatus=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "incentiveStatus": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/walmart/latest/actions/list-price-incentive-items?${params}`, {
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
| `incentiveStatus` | list<string> | yes |  |
| `incentiveType` | list<string> | no |  |
| `sortBy` | string | no |  |
| `sortOrder` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "baseReferralFee": 1,
      "currentPrice": 1,
      "enrollmentDate": "string",
      "enrollmentType": "string",
      "expirationDate": "string",
      "incentiveId": "string",
      "incentiveStatus": "string",
      "incentiveType": "string",
      "inventoryCount": "string",
      "itemId": "string",
      "productImageUrl": "https://example.com",
      "productName": "Ava Chen",
      "productUrl": "https://example.com",
      "reducedReferralFee": 1,
      "shippingPrice": 1,
      "skuId": "string",
      "startDate": "string",
      "targetPrice": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `baseReferralFee` | number |  |
| `currentPrice` | number |  |
| `enrollmentDate` | string |  |
| `enrollmentType` | string |  |
| `expirationDate` | string |  |
| `incentiveId` | string |  |
| `incentiveStatus` | string |  |
| `incentiveType` | string |  |
| `inventoryCount` | string |  |
| `itemId` | string |  |
| `productImageUrl` | string |  |
| `productName` | string |  |
| `productUrl` | string |  |
| `reducedReferralFee` | number |  |
| `shippingPrice` | number |  |
| `skuId` | string |  |
| `startDate` | string |  |
| `targetPrice` | number |  |

## Native endpoint

Through the native Walmart API, this operation is `GET /v3/price/incentives` (base URL `https://{{credentials.environment}}.walmartapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-price-incentive-items.md) for the provider-specific parameters and requirements.

