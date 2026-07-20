# SuperMCP: Create Campaign



```
POST https://connect.mindcloud.co/v1/universal/superMCP/latest/actions/create-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SuperMCP `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/superMCP/latest/actions/create-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "dataSourceId": "string",
  "accountId": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/superMCP/latest/actions/create-campaign', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "dataSourceId": "string",
    "accountId": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `dataSourceId` | string | yes | Ad platform data source code: AW, FA, AC, TIK, or LIA. |
| `accountId` | string | yes | Platform ad account ID from Discover Accounts. |
| `name` | string | yes | Campaign name. |
| `status` | string | no | Campaign status. Supermetrics creates campaigns as PAUSED for safe review. Default: `PAUSED`. |
| `budgetAmount` | number | no | Budget amount in account currency. |
| `budgetType` | string | no | Budget type such as DAILY or LIFETIME. |
| `startDate` | date | no | Campaign start date in YYYY-MM-DD format. |
| `endDate` | date | no | Campaign end date in YYYY-MM-DD format. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `targeting` | object | no | Campaign-level targeting object. |
| `platformSettings` | object | no | Platform-specific campaign settings. |
| `biddingStrategy` | string | no | Platform bidding strategy. |
| `adGroups[]` | array<object> | no | Ad groups or ad sets to create with the campaign. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "notes": [
        "string"
      ],
      "results": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `notes` | array<string> | Creation notes or partial success details. |
| `results` | array<object> | Created campaign results. |

## Native endpoint

Through the native SuperMCP API, this operation is `POST /mcp/campaign_create` (base URL `https://mcp.supermetrics.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-campaign.md) for the provider-specific parameters and requirements.

