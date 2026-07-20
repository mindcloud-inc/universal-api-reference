# Instantly: Get Daily Campaign Analytics

Retrieves daily campaign analytics from Instantly.

```
GET https://connect.mindcloud.co/v1/universal/instantly/latest/actions/get-daily-campaign-analytics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instantly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instantly/latest/actions/get-daily-campaign-analytics?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instantly/latest/actions/get-daily-campaign-analytics?${params}`, {
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
| `campaignId` | string | no | Campaign ID for daily analytics. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bounced_count": 1,
      "campaign_id": "string",
      "date": "2026-05-07T12:00:00.000Z",
      "emails_sent_count": 1,
      "link_click_count": 1,
      "open_count": 1,
      "reply_count": 1,
      "unsubscribed_count": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bounced_count` | number |  |
| `campaign_id` | string |  |
| `date` | date |  |
| `emails_sent_count` | number |  |
| `link_click_count` | number |  |
| `open_count` | number |  |
| `reply_count` | number |  |
| `unsubscribed_count` | number |  |

## Native endpoint

Through the native Instantly API, this operation is `GET /api/v2/campaigns/analytics/daily` (base URL `https://api.instantly.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-daily-campaign-analytics.md) for the provider-specific parameters and requirements.

