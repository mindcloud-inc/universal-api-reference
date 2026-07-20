# SeaX: Delete Auto Dialer Campaign

Deletes an auto dialer campaign from SeaX.

```
DELETE https://connect.mindcloud.co/v1/universal/seaX/latest/actions/delete-auto-dialer-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SeaX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/seaX/latest/actions/delete-auto-dialer-campaign?connectionId=$CONNECTION_ID&autoDialerCampaignId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "autoDialerCampaignId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seaX/latest/actions/delete-auto-dialer-campaign?${params}`, {
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
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native SeaX API, this operation is `DELETE /auto_dialer_campaigns/{auto_dialer_campaign_id}` (base URL `https://seax.seasalt.ai/seax-api/api/v1/workspace/{{credentials.workspaceId}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-auto-dialer-campaign.md) for the provider-specific parameters and requirements.

