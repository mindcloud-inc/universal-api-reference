# Moderation API: Get Queue Statistics

Retrieves review queue statistics from Moderation API.

```
GET https://connect.mindcloud.co/v1/universal/moderationAPI/latest/actions/get-queue-statistics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moderation API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moderationAPI/latest/actions/get-queue-statistics?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moderationAPI/latest/actions/get-queue-statistics?${params}`, {
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
| `id` | string | yes | The queue ID |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `withinDays` | string | no | Number of days to analyze statistics for |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actionStats": [
        {}
      ],
      "reviewStats": {},
      "topReviewers": [
        {}
      ],
      "trends": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actionStats` | array<object> |  |
| `reviewStats` | object |  |
| `topReviewers` | array<object> | List of top reviewers and their statistics |
| `trends` | object |  |

## Native endpoint

Through the native Moderation API API, this operation is `GET /queue/:id/stats` (base URL `https://api.moderationapi.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-queue-statistics.md) for the provider-specific parameters and requirements.

