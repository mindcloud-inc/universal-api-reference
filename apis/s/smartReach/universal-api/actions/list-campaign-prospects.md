# SmartReach: List Campaign Prospects

Retrieves campaign prospects from SmartReach.

```
GET https://connect.mindcloud.co/v1/universal/smartReach/latest/actions/list-campaign-prospects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SmartReach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartReach/latest/actions/list-campaign-prospects?connectionId=$CONNECTION_ID&campaignId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaignId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartReach/latest/actions/list-campaign-prospects?${params}`, {
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
| `campaignId` | string | yes | ID of campaign to return |
| `olderThan` | number | no | timestamp in unix epoch milliseconds |
| `newerThan` | number | no | timestamp in unix epoch milliseconds |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaign_prospects": [
        {
          "prospect_status_in_campaign": {
            "campaign_id": "string"
          },
          "prospect": {
            "emails": [
              {
                "email": "ava@example.com"
              }
            ],
            "id": "string"
          }
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaign_prospects[].prospect_status_in_campaign.campaign_id` | string |  |
| `campaign_prospects[].prospect.emails[].email` | string |  |
| `campaign_prospects[].prospect.id` | string |  |

## Native endpoint

Through the native SmartReach API, this operation is `GET /campaigns/:campaign_id/prospects` (base URL `https://api.smartreach.io/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-campaign-prospects.md) for the provider-specific parameters and requirements.

