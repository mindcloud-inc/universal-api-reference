# Ringg AI: Get Drill-Down Analytics

Retrieves drill-down analytics from Ringg AI.

```
GET https://connect.mindcloud.co/v1/universal/ringgAI/latest/actions/get-drill-down-analytics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ringg AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ringgAI/latest/actions/get-drill-down-analytics?connectionId=$CONNECTION_ID&bulkListId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "bulkListId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ringgAI/latest/actions/get-drill-down-analytics?${params}`, {
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
| `bulkListId` | string | yes | (Required) Bulk list/campaign ID to get drill-down analytics for |
| `startDate` | string | no | Start date for analytics filter (YYYY-MM-DD format) |
| `endDate` | string | no | End date for analytics filter (YYYY-MM-DD format) |
| `agentId` | string | no | Filter by specific agent ID |
| `voicemail` | boolean | no | Filter by voicemail status |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cached": true,
      "performanceMetrics": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cached` | boolean | Whether the response was served from cache |
| `performanceMetrics` | object | Detailed performance metrics for the bulk list |

## Native endpoint

Through the native Ringg AI API, this operation is `GET /analytics/drill-down-analytics` (base URL `https://prod-api.ringg.ai/ca/api/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-drill-down-analytics.md) for the provider-specific parameters and requirements.

