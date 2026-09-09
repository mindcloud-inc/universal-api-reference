# Walmart: Get Campaign Details

Retrieve detailed information about a specific Campaign. Provide the Campaign's unique ID in the request to fetch its attributes.

```
GET https://connect.mindcloud.co/v1/universal/walmart/latest/actions/get-campaign-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Walmart `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/walmart/latest/actions/get-campaign-details?connectionId=$CONNECTION_ID&campaignId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaignId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/walmart/latest/actions/get-campaign-details?${params}`, {
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
| `campaignId` | string | yes | Campaign ID of the campaign whose details are to be retrieved. |

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

Through the native Walmart API, this operation is `GET v3/advertising/sem/campaigns/:campaignId` (base URL `https://{{credentials.environment}}.walmartapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-campaign-details.md) for the provider-specific parameters and requirements.

