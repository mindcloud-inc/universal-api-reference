# SEOTakeoff: Score Article Quality



```
GET https://connect.mindcloud.co/v1/universal/sEOTakeoff/latest/actions/score-article-quality
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SEOTakeoff `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sEOTakeoff/latest/actions/score-article-quality?connectionId=$CONNECTION_ID&content=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "content": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sEOTakeoff/latest/actions/score-article-quality?${params}`, {
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
| `content` | string | yes | Article content to score. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `metadata` | object | no | Optional metadata object to include with scoring. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "breakdown": {},
      "grade": "string",
      "overall_score": 1,
      "passed": true,
      "recommendations": [
        "string"
      ],
      "scored_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `breakdown` | object |  |
| `grade` | string |  |
| `overall_score` | number |  |
| `passed` | boolean |  |
| `recommendations` | array<string> |  |
| `scored_at` | date |  |

## Native endpoint

Through the native SEOTakeoff API, this operation is `POST /api/v1/quality/score` (base URL `https://api.seotakeoff.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/score-article-quality.md) for the provider-specific parameters and requirements.

