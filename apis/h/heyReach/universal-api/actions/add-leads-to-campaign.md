# Hey Reach: Add Leads To Campaign

Adds leads to a campaign in Hey Reach.

```
PUT https://connect.mindcloud.co/v1/universal/heyReach/latest/actions/add-leads-to-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hey Reach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/heyReach/latest/actions/add-leads-to-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "campaignId": 1,
  "accountLeadPairs[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/heyReach/latest/actions/add-leads-to-campaign', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "campaignId": 1,
    "accountLeadPairs[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `campaignId` | number | yes |  |
| `accountLeadPairs[]` | array<object> | yes |  |
| `resumeFinishedCampaign` | boolean | no |  |
| `resumePausedCampaign` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addedLeadsCount": 1,
      "failedLeadsCount": 1,
      "updatedLeadsCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addedLeadsCount` | number |  |
| `failedLeadsCount` | number |  |
| `updatedLeadsCount` | number |  |

## Native endpoint

Through the native Hey Reach API, this operation is `POST /api/public/campaign/AddLeadsToCampaignV2` (base URL `https://api.heyreach.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-leads-to-campaign.md) for the provider-specific parameters and requirements.

