# Instantly: Get Campaign Analytics Overview

Retrieves campaign analytics overview from Instantly.

```
GET https://connect.mindcloud.co/v1/universal/instantly/latest/actions/get-campaign-analytics-overview
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instantly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instantly/latest/actions/get-campaign-analytics-overview?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instantly/latest/actions/get-campaign-analytics-overview?${params}`, {
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
| `id` | string | no | Campaign ID for analytics overview. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bounced_count": 1,
      "contacted_count": 1,
      "emails_sent_count": 1,
      "link_click_count": 1,
      "open_count": 1,
      "open_count_unique": 1,
      "reply_count": 1,
      "total_opportunities": 1,
      "total_opportunity_value": 1,
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
| `contacted_count` | number |  |
| `emails_sent_count` | number |  |
| `link_click_count` | number |  |
| `open_count` | number |  |
| `open_count_unique` | number |  |
| `reply_count` | number |  |
| `total_opportunities` | number |  |
| `total_opportunity_value` | number |  |
| `unsubscribed_count` | number |  |

## Native endpoint

Through the native Instantly API, this operation is `GET /api/v2/campaigns/analytics/overview` (base URL `https://api.instantly.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-campaign-analytics-overview.md) for the provider-specific parameters and requirements.

