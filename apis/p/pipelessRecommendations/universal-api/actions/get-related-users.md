# Pipeless Recommendations: Get Related Users

Retrieves related users in Pipeless Recommendations.

```
GET https://connect.mindcloud.co/v1/universal/pipelessRecommendations/latest/actions/get-related-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pipeless Recommendations `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pipelessRecommendations/latest/actions/get-related-users?connectionId=$CONNECTION_ID&appId=1885&object.id=33&object.type=user&followedRelationshipType=followed&contentTaggedRelationshipType=categorizedIn" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "appId": "1885",
  "object.id": "33",
  "object.type": "user",
  "followedRelationshipType": "followed",
  "contentTaggedRelationshipType": "categorizedIn"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pipelessRecommendations/latest/actions/get-related-users?${params}`, {
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
| `followedRelationshipType` | string | yes | Default: `followed`. |
| `contentTaggedRelationshipType` | string | yes | Default: `categorizedIn`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
        {
          "object": {
            "createdOn": "2026-05-07T12:00:00.000Z",
            "id": "string",
            "modifiedOn": "2026-05-07T12:00:00.000Z",
            "type": "string"
          }
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
| `items[].object.createdOn` | date |  |
| `items[].object.id` | string |  |
| `items[].object.modifiedOn` | date |  |
| `items[].object.type` | string |  |

## Native endpoint

Through the native Pipeless Recommendations API, this operation is `GET /v1/apps/:appId/algos/recommendations/related-users` (base URL `https://api.pipeless.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-related-users.md) for the provider-specific parameters and requirements.

