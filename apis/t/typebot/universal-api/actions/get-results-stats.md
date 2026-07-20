# Typebot: Get Results Stats



```
GET https://connect.mindcloud.co/v1/universal/typebot/latest/actions/get-results-stats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Typebot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/typebot/latest/actions/get-results-stats?connectionId=$CONNECTION_ID&typebotId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "typebotId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/typebot/latest/actions/get-results-stats?${params}`, {
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
| `typebotId` | string | yes | The Typebot ID. |
| `timeFilter` | string | no | Time range filter. |
| `timeZone` | string | no | Time zone for the time filter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "totalCompleted": 1,
      "totalStarts": 1,
      "totalViews": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `totalCompleted` | number |  |
| `totalStarts` | number |  |
| `totalViews` | number |  |

## Native endpoint

Through the native Typebot API, this operation is `GET /v1/typebots/:typebotId/analytics/stats` (base URL `https://app.typebot.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-results-stats.md) for the provider-specific parameters and requirements.

