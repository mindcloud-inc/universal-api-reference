# SmartReach: Update Prospect Status

Updates prospect status in SmartReach.

```
PUT https://connect.mindcloud.co/v1/universal/smartReach/latest/actions/update-prospect-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SmartReach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/smartReach/latest/actions/update-prospect-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "campaignIds[]": [
    "string"
  ],
  "prospectIds[]": [
    "string"
  ],
  "prospectStatus": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/smartReach/latest/actions/update-prospect-status', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "campaignIds[]": ["string"],
    "prospectIds[]": ["string"],
    "prospectStatus": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `campaignIds[]` | array<string> | yes | Campaign IDs associated with the prospect status update. |
| `prospectIds[]` | array<string> | yes | Prospect IDs to update. |
| `prospectStatus` | string | yes | Target prospect status to apply. |
| `willResumeAt` | number | no | Resume timestamp when using resume_later. |
| `willResumeAtTz` | string | no | Timezone for the resume timestamp. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "prospect_status_updated": [
        {
          "prospect_status_in_campaign": {
            "campaign_id": "string"
          },
          "prospect": {
            "id": "string"
          }
        }
      ],
      "total_updated": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `prospect_status_updated[].prospect_status_in_campaign.campaign_id` | string |  |
| `prospect_status_updated[].prospect.id` | string |  |
| `total_updated` | number |  |

## Native endpoint

Through the native SmartReach API, this operation is `PUT /prospects/prospect_status_change` (base URL `https://api.smartreach.io/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-prospect-status.md) for the provider-specific parameters and requirements.

