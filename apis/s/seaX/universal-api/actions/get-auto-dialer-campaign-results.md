# SeaX: Get Auto Dialer Campaign Results

Retrieves structured results for a SeaX auto dialer campaign.

```
GET https://connect.mindcloud.co/v1/universal/seaX/latest/actions/get-auto-dialer-campaign-results
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SeaX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seaX/latest/actions/get-auto-dialer-campaign-results?connectionId=$CONNECTION_ID&autoDialerCampaignId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "autoDialerCampaignId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seaX/latest/actions/get-auto-dialer-campaign-results?${params}`, {
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
| `autoDialerCampaignId` | string | yes | Auto dialer campaign identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ai_agent_id": "string",
      "ai_agent_name": "Ava Chen",
      "campaign_id": "string",
      "campaign_name": "Ava Chen",
      "campaign_results": [
        {}
      ],
      "campaign_status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ai_agent_id` | string |  |
| `ai_agent_name` | string |  |
| `campaign_id` | string |  |
| `campaign_name` | string |  |
| `campaign_results` | array<object> |  |
| `campaign_status` | string |  |

## Native endpoint

Through the native SeaX API, this operation is `GET /auto_dialer_campaigns/{auto_dialer_campaign_id}/results` (base URL `https://seax.seasalt.ai/seax-api/api/v1/workspace/{{credentials.workspaceId}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-auto-dialer-campaign-results.md) for the provider-specific parameters and requirements.

