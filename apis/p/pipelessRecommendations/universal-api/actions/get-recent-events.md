# Pipeless Recommendations: Get Recent Events

Retrieves recent events from Pipeless Recommendations.

```
GET https://connect.mindcloud.co/v1/universal/pipelessRecommendations/latest/actions/get-recent-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pipeless Recommendations `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pipelessRecommendations/latest/actions/get-recent-events?connectionId=$CONNECTION_ID&appId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "appId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pipelessRecommendations/latest/actions/get-recent-events?${params}`, {
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
| `appId` | string | yes | Numeric Pipeless app ID for the target recommendation app. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "event": {
        "endObject": {
          "createdOn": "2026-05-07T12:00:00.000Z",
          "id": "string",
          "modifiedOn": "2026-05-07T12:00:00.000Z",
          "type": "string"
        },
        "relationship": {
          "createdOn": "2026-05-07T12:00:00.000Z",
          "type": "string"
        },
        "startObject": {
          "createdOn": "2026-05-07T12:00:00.000Z",
          "id": "string",
          "modifiedOn": "2026-05-07T12:00:00.000Z",
          "type": "string"
        }
      },
      "eventAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `event.endObject.createdOn` | date |  |
| `event.endObject.id` | string |  |
| `event.endObject.modifiedOn` | date |  |
| `event.endObject.type` | string |  |
| `event.relationship.createdOn` | date |  |
| `event.relationship.type` | string |  |
| `event.startObject.createdOn` | date |  |
| `event.startObject.id` | string |  |
| `event.startObject.modifiedOn` | date |  |
| `event.startObject.type` | string |  |
| `eventAt` | date | When the event occurred. |

## Native endpoint

Through the native Pipeless Recommendations API, this operation is `GET /v1/apps/:appId/recent-events` (base URL `https://api.pipeless.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-recent-events.md) for the provider-specific parameters and requirements.

