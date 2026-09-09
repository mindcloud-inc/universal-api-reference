# Walmart: Create Campaign

This API allows you to create a new Campaign.

```
POST https://connect.mindcloud.co/v1/universal/walmart/latest/actions/create-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Walmart `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/walmart/latest/actions/create-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/walmart/latest/actions/create-campaign', {
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
| `itemsOperations.operationType` | list<string> | no | Type of operation to perform on campaign Items. Allowed Values: `ADD`, `REMOVE` |
| `metadata` | object | no | Metadata for the campaign. |
| `metadata.name` | string | no | Name of the campaign. Allowed characters: letters, digits, dashes, underscores, and spaces. Maximum 255 characters allowed. |
| `itemsOperations` | object | no | List of Operations to perform on campaign items. |
| `itemsOperations.skus[]` | array<string> | no |  |
| `metadata.startDate` | string | no | Start date of the campaign in yyyy-MM-dd format. |
| `metadata.endDate` | string | no | End date of the campaign in yyyy-MM-dd format. |
| `metadata.dailyBudget` | number | no | Daily budget allocated for the campaign. Must be a positive value with up to 2 decimal places. Daily budget must be between $5.00 and $2,500.00. |
| `metadata.totalBudget` | number | no | (optional) Total budget allocated for the campaign. Must be a positive value with up to 2 decimal places. Total budget must be between $5.00 and $250,000.00. Total budget must be greater than or equal to daily budget. |
| `metadata.biddingStrategyType` | list<string> | no | Bidding strategy type for the campaign. Defaults to `TARGET_ROAS` if not specified. |
| `metadata.targetRoas` | number | no | Target ROAS for the campaign. Must be a positive value between 1.00 and 20.00, with up to 2 decimal places. Defaults to `3.5` if not specified. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaignId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaignId` | string |  |

## Native endpoint

Through the native Walmart API, this operation is `POST v3/advertising/sem/campaigns` (base URL `https://{{credentials.environment}}.walmartapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-campaign.md) for the provider-specific parameters and requirements.

