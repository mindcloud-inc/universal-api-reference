# Countly: Get Analytics Events

Retrieves all analytics events from Countly.

```
GET https://connect.mindcloud.co/v1/universal/countly/latest/actions/get-analytics-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Countly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/countly/latest/actions/get-analytics-events?connectionId=$CONNECTION_ID&appId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "appId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/countly/latest/actions/get-analytics-events?${params}`, {
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
| `appId` | string | yes | Countly app ID to query analytics for. |
| `period` | string | no | Countly reporting period, such as month, 60days, 30days, 7days, yesterday, or today. |
| `event` | string | no | Event key to query. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `events` | string | no | JSON string array of event keys to query together. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Analytics events response keyed by event and period. |

## Native endpoint

Through the native Countly API, this operation is `GET /o/analytics/events` (base URL `https://mindcloud-fe49f15890040.flex.countly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-analytics-events.md) for the provider-specific parameters and requirements.

