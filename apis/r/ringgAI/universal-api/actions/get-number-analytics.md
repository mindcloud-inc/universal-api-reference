# Ringg AI: Get Number Analytics

Retrieves number analytics from Ringg AI.

```
GET https://connect.mindcloud.co/v1/universal/ringgAI/latest/actions/get-number-analytics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ringg AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ringgAI/latest/actions/get-number-analytics?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ringgAI/latest/actions/get-number-analytics?${params}`, {
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
| `startDate` | string | no | Start date for analytics filter (YYYY-MM-DD format) |
| `endDate` | string | no | End date for analytics filter (YYYY-MM-DD format) |
| `agentId` | string | no | Filter by specific agent ID |
| `bulkListId` | string | no | Filter by specific bulk list/campaign ID |
| `voicemail` | boolean | no | Filter by voicemail status |

## Response

```json
{
  "success": true,
  "data": [
    {
      "numberAnalytics": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `numberAnalytics` | array<string> | Analytics data grouped by phone numbers |

## Native endpoint

Through the native Ringg AI API, this operation is `GET /analytics/number-analytics` (base URL `https://prod-api.ringg.ai/ca/api/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-number-analytics.md) for the provider-specific parameters and requirements.

