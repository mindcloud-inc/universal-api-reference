# SmartReach: Add Prospects To Campaign

Adds prospects to a campaign in SmartReach.

```
POST https://connect.mindcloud.co/v1/universal/smartReach/latest/actions/add-prospects-to-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SmartReach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/smartReach/latest/actions/add-prospects-to-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "campaignId": "string",
  "prospectIds[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/smartReach/latest/actions/add-prospects-to-campaign', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "campaignId": "string",
    "prospectIds[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `campaignId` | string | yes | ID of campaign to return |
| `prospectIds[]` | array<string> | yes | Prospect IDs to add to the campaign. |
| `ignoreProspectsInOtherCampaigns` | string | no | How to handle prospects already present in other campaigns. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaign_id": "string",
      "prospect_data": [
        {
          "id": "string"
        }
      ],
      "total_assigned": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaign_id` | string |  |
| `prospect_data[].id` | string |  |
| `total_assigned` | number |  |

## Native endpoint

Through the native SmartReach API, this operation is `POST /campaigns/:campaign_id/prospects` (base URL `https://api.smartreach.io/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-prospects-to-campaign.md) for the provider-specific parameters and requirements.

