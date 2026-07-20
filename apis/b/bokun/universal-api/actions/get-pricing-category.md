# Bokun: Get Pricing Category

Retrieves a pricing category by ID from Bokun.

```
GET https://connect.mindcloud.co/v1/universal/bokun/latest/actions/get-pricing-category
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bokun `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bokun/latest/actions/get-pricing-category?connectionId=$CONNECTION_ID&pricingCategoryId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "pricingCategoryId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bokun/latest/actions/get-pricing-category?${params}`, {
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
| `pricingCategoryId` | number | yes | The Bokun pricing category ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ageQualified": true,
      "dependent": true,
      "groupSize": 1,
      "id": 1,
      "internalUseOnly": true,
      "masterCategoryId": 1,
      "maxAge": 1,
      "maxDependentSum": 1,
      "maxPerMaster": 1,
      "minAge": 1,
      "occupancy": 1,
      "sumDependentCategories": true,
      "ticketCategory": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ageQualified` | boolean |  |
| `dependent` | boolean |  |
| `groupSize` | number |  |
| `id` | number |  |
| `internalUseOnly` | boolean |  |
| `masterCategoryId` | number |  |
| `maxAge` | number |  |
| `maxDependentSum` | number |  |
| `maxPerMaster` | number |  |
| `minAge` | number |  |
| `occupancy` | number |  |
| `sumDependentCategories` | boolean |  |
| `ticketCategory` | string |  |
| `title` | string |  |

## Native endpoint

Through the native Bokun API, this operation is `GET /restapi/v2.0/pricing/category/:pricingCategoryId` (base URL `https://api.bokun.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-pricing-category.md) for the provider-specific parameters and requirements.

