# SuperMCP: Update Campaign



```
PUT https://connect.mindcloud.co/v1/universal/superMCP/latest/actions/update-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SuperMCP `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/superMCP/latest/actions/update-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "dataSourceId": "string",
  "accountId": "string",
  "campaignId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/superMCP/latest/actions/update-campaign', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "dataSourceId": "string",
    "accountId": "string",
    "campaignId": "string"
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
| `campaignId` | string | yes | Campaign ID to update. |
| `name` | string | no | Updated campaign name. |
| `status` | string | no | Updated campaign status. |
| `budgetAmount` | number | no | Updated budget amount in account currency. |
| `budgetType` | string | no | Updated budget type such as DAILY or LIFETIME. |
| `startDate` | date | no | Updated campaign start date. |
| `endDate` | date | no | Updated campaign end date. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `targeting` | object | no | Updated targeting object. |
| `platformSettings` | object | no | Updated platform-specific settings. |
| `biddingStrategy` | string | no | Updated bidding strategy. |
| `adGroups[]` | array<object> | no | Ad groups or ad sets to add/update. |

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
| `notes` | array<string> | Update notes or partial success details. |
| `results` | array<object> | Updated campaign results. |

## Native endpoint

Through the native SuperMCP API, this operation is `POST /mcp/campaign_update` (base URL `https://mcp.supermetrics.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-campaign.md) for the provider-specific parameters and requirements.

