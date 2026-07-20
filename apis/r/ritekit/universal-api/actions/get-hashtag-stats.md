# Ritekit: Get Hashtag Stats

Retrieves real-time stats for Ritekit hashtags.

```
GET https://connect.mindcloud.co/v1/universal/ritekit/latest/actions/get-hashtag-stats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ritekit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ritekit/latest/actions/get-hashtag-stats?connectionId=$CONNECTION_ID&tags=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tags": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ritekit/latest/actions/get-hashtag-stats?${params}`, {
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
| `tags` | string | yes | Comma-separated hashtags to analyze. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "color": [
        "string"
      ],
      "hashtags": [
        "string"
      ],
      "message": "string",
      "result": true,
      "stats": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `color` | array<string> |  |
| `hashtags` | array<string> |  |
| `message` | string |  |
| `result` | boolean |  |
| `stats` | array<object> |  |

## Native endpoint

Through the native Ritekit API, this operation is `GET /v1/stats/multiple-hashtags` (base URL `https://api.ritekit.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-hashtag-stats.md) for the provider-specific parameters and requirements.

