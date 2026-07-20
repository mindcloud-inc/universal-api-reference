# Campaign Monitor: Get Campaign Summary

Retrieves summary metrics for a sent Campaign Monitor campaign.

```
GET https://connect.mindcloud.co/v1/universal/campaignMonitor/latest/actions/get-campaign-summary
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Campaign Monitor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/campaignMonitor/latest/actions/get-campaign-summary?connectionId=$CONNECTION_ID&campaignId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaignId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/campaignMonitor/latest/actions/get-campaign-summary?${params}`, {
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
| `campaignId` | string | yes | Campaign Monitor campaign identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bounced": 1,
      "clicks": 1,
      "forwards": 1,
      "likes": 1,
      "mentions": 1,
      "name": "Ava Chen",
      "recipients": 1,
      "spamComplaints": 1,
      "totalOpened": 1,
      "uniqueOpened": 1,
      "unsubscribed": 1,
      "webVersionTextUrl": "https://example.com",
      "webVersionUrl": "https://example.com",
      "worldviewUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bounced` | number | Total bounces recorded for the campaign. |
| `clicks` | number | Total clicks recorded for the campaign. |
| `forwards` | number | Total forwards recorded for the campaign. |
| `likes` | number | Total likes recorded for the campaign. |
| `mentions` | number | Total social mentions recorded for the campaign. |
| `name` | string | Campaign name. |
| `recipients` | number | Total recipients in the campaign. |
| `spamComplaints` | number | Spam complaints recorded for the campaign. |
| `totalOpened` | number | Total opens recorded for the campaign. |
| `uniqueOpened` | number | Unique opens recorded for the campaign. |
| `unsubscribed` | number | Total unsubscribes recorded for the campaign. |
| `webVersionTextUrl` | string | Hosted plain-text version URL for the campaign. |
| `webVersionUrl` | string | Hosted web version URL for the campaign. |
| `worldviewUrl` | string | Campaign Monitor Worldview report URL. |

## Native endpoint

Through the native Campaign Monitor API, this operation is `GET /campaigns/:campaignId/summary.json` (base URL `https://api.createsend.com/api/v3.3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-campaign-summary.md) for the provider-specific parameters and requirements.

