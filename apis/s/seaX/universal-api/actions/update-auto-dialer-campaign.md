# SeaX: Update Auto Dialer Campaign

Updates an auto dialer campaign in SeaX.

```
PUT https://connect.mindcloud.co/v1/universal/seaX/latest/actions/update-auto-dialer-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SeaX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/seaX/latest/actions/update-auto-dialer-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "autoDialerCampaignId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/seaX/latest/actions/update-auto-dialer-campaign', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "autoDialerCampaignId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `autoDialerCampaignId` | string | yes | Auto dialer campaign identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_time": "string",
      "id": "string",
      "message": "string",
      "name": "Ava Chen",
      "type": {},
      "updated_time": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_time` | string |  |
| `id` | string |  |
| `message` | string |  |
| `name` | string |  |
| `type` | object |  |
| `updated_time` | string |  |

## Native endpoint

Through the native SeaX API, this operation is `PATCH /auto_dialer_campaigns/{auto_dialer_campaign_id}` (base URL `https://seax.seasalt.ai/seax-api/api/v1/workspace/{{credentials.workspaceId}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-auto-dialer-campaign.md) for the provider-specific parameters and requirements.

