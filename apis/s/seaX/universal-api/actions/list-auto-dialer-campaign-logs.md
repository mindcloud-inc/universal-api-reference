# SeaX: List Auto Dialer Campaign Logs

Retrieves logs for a SeaX auto dialer campaign.

```
GET https://connect.mindcloud.co/v1/universal/seaX/latest/actions/list-auto-dialer-campaign-logs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SeaX `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seaX/latest/actions/list-auto-dialer-campaign-logs?connectionId=$CONNECTION_ID&limit=25&offset=0&autoDialerCampaignId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "autoDialerCampaignId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seaX/latest/actions/list-auto-dialer-campaign-logs?${params}`, {
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
      "data": [
        {}
      ],
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | Auto dialer campaign log entries. |
| `total` | number | Total number of log entries. |

## Native endpoint

Through the native SeaX API, this operation is `GET /auto_dialer_campaigns/{auto_dialer_campaign_id}/logs` (base URL `https://seax.seasalt.ai/seax-api/api/v1/workspace/{{credentials.workspaceId}}`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-auto-dialer-campaign-logs.md) for the provider-specific parameters and requirements.

