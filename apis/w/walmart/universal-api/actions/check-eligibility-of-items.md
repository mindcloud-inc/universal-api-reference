# Walmart: Check Eligibility of Items

Check whether an item from your catalog meets the required conditions for Search Engine Marketing ads.

```
GET https://connect.mindcloud.co/v1/universal/walmart/latest/actions/check-eligibility-of-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Walmart `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/walmart/latest/actions/check-eligibility-of-items?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/walmart/latest/actions/check-eligibility-of-items?${params}`, {
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
| `filters[]` | array<object> | no |  |
| `filters[].field` | string | no |  |
| `filters[].values[]` | array<string> | no |  |

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

Through the native Walmart API, this operation is `POST v3/advertising/sem/items/eligibility` (base URL `https://{{credentials.environment}}.walmartapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-eligibility-of-items.md) for the provider-specific parameters and requirements.

