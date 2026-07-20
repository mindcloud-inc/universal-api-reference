# Countly: List Events

Retrieves all events from Countly.

```
GET https://connect.mindcloud.co/v1/universal/countly/latest/actions/list-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Countly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/countly/latest/actions/list-events?connectionId=$CONNECTION_ID&appId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "appId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/countly/latest/actions/list-events?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "events": {},
      "limits": {
        "event_limit": 1,
        "event_segmentation_limit": 1,
        "event_segmentation_value_limit": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `events` | object | Event map when Countly has tracked events for the app. |
| `limits.event_limit` | number |  |
| `limits.event_segmentation_limit` | number |  |
| `limits.event_segmentation_value_limit` | number |  |

## Native endpoint

Through the native Countly API, this operation is `GET /o` (base URL `https://mindcloud-fe49f15890040.flex.countly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-events.md) for the provider-specific parameters and requirements.

