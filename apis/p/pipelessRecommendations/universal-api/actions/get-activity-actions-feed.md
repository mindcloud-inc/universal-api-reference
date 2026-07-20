# Pipeless Recommendations: Get Activity Actions Feed

Retrieves grouped activity actions for an object in Pipeless Recommendations.

```
GET https://connect.mindcloud.co/v1/universal/pipelessRecommendations/latest/actions/get-activity-actions-feed
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pipeless Recommendations `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pipelessRecommendations/latest/actions/get-activity-actions-feed?connectionId=$CONNECTION_ID&appId=1885&object.id=33&object.type=user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "appId": "1885",
  "object.id": "33",
  "object.type": "user"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pipelessRecommendations/latest/actions/get-activity-actions-feed?${params}`, {
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
| `object.id` | string | yes | Default: `33`. |
| `object.type` | string | yes | Default: `user`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "events": [
        {
          "actionObject": {
            "createdOn": "2026-05-07T12:00:00.000Z",
            "id": "string",
            "modifiedOn": "2026-05-07T12:00:00.000Z",
            "type": "string"
          },
          "actions": [
            {
              "actionRelationship": {
                "createdOn": "2026-05-07T12:00:00.000Z",
                "type": "string"
              },
              "actorObject": {
                "createdOn": "2026-05-07T12:00:00.000Z",
                "id": "string",
                "modifiedOn": "2026-05-07T12:00:00.000Z",
                "type": "string"
              }
            }
          ]
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `events[].actionObject.createdOn` | date |  |
| `events[].actionObject.id` | string |  |
| `events[].actionObject.modifiedOn` | date |  |
| `events[].actionObject.type` | string |  |
| `events[].actions[].actionRelationship.createdOn` | date |  |
| `events[].actions[].actionRelationship.type` | string |  |
| `events[].actions[].actorObject.createdOn` | date |  |
| `events[].actions[].actorObject.id` | string |  |
| `events[].actions[].actorObject.modifiedOn` | date |  |
| `events[].actions[].actorObject.type` | string |  |

## Native endpoint

Through the native Pipeless Recommendations API, this operation is `GET /v1/apps/:appId/algos/activity/actions-feed` (base URL `https://api.pipeless.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-activity-actions-feed.md) for the provider-specific parameters and requirements.

