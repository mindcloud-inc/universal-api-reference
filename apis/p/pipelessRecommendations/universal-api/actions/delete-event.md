# Pipeless Recommendations: Delete Event

Deletes one or more events from Pipeless Recommendations.

```
DELETE https://connect.mindcloud.co/v1/universal/pipelessRecommendations/latest/actions/delete-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pipeless Recommendations `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/pipelessRecommendations/latest/actions/delete-event?connectionId=$CONNECTION_ID&appId=1885" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "appId": "1885"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pipelessRecommendations/latest/actions/delete-event?${params}`, {
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
| `appId` | string | yes | Numeric Pipeless app ID. Default: `1885`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | Whether the delete request succeeded. |

## Native endpoint

Through the native Pipeless Recommendations API, this operation is `DELETE /v1/apps/:appId/events` (base URL `https://api.pipeless.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-event.md) for the provider-specific parameters and requirements.

