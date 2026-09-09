# Walmart: Get Top Recommended Catalog Items

This API allows you to fetch a list of top recommended items from your catalog.

```
GET https://connect.mindcloud.co/v1/universal/walmart/latest/actions/get-top-recommended-catalog-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Walmart `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/walmart/latest/actions/get-top-recommended-catalog-items?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/walmart/latest/actions/get-top-recommended-catalog-items?${params}`, {
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
| `limit` | number | no | # of records to retrieve. Default: `100`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "biddingStrategyType": "string",
      "campaignId": "string",
      "createdDate": "string",
      "dailyBudget": 1,
      "endDate": "string",
      "name": "Ava Chen",
      "startDate": "string",
      "status": "string",
      "targetRoas": 1,
      "totalBudget": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `biddingStrategyType` | string |  |
| `campaignId` | string |  |
| `createdDate` | string |  |
| `dailyBudget` | number |  |
| `endDate` | string |  |
| `name` | string |  |
| `startDate` | string |  |
| `status` | string |  |
| `targetRoas` | number |  |
| `totalBudget` | number |  |

## Native endpoint

Through the native Walmart API, this operation is `GET v3/advertising/sem/items/recommendations` (base URL `https://{{credentials.environment}}.walmartapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-top-recommended-catalog-items.md) for the provider-specific parameters and requirements.

