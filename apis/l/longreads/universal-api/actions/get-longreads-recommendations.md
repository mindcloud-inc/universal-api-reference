# Longreads: Get Longreads Recommendations

Retrieves Longreads article recommendations by topic.

```
GET https://connect.mindcloud.co/v1/universal/longreads/latest/actions/get-longreads-recommendations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Longreads `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/longreads/latest/actions/get-longreads-recommendations?connectionId=$CONNECTION_ID&topics=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "topics": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/longreads/latest/actions/get-longreads-recommendations?${params}`, {
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
| `topics` | string | yes | Comma-separated topics such as books or climate. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "recommendations": [
        {}
      ],
      "tags_matched": [
        "string"
      ],
      "topics": [
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
| `count` | number |  |
| `recommendations` | array<object> |  |
| `tags_matched` | array<string> |  |
| `topics` | array<string> |  |

## Native endpoint

Through the native Longreads API, this operation is `GET /longreads/v1/recommendations` (base URL `https://longreads.com/wp-json`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-longreads-recommendations.md) for the provider-specific parameters and requirements.

