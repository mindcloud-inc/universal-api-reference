# Winston AI: Compare Text



```
GET https://connect.mindcloud.co/v1/universal/winstonAI/latest/actions/compare-text
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Winston AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/winstonAI/latest/actions/compare-text?connectionId=$CONNECTION_ID&firstText=Text%20to%20compare%20against%20the%20second%20input&secondText=Second%20text%20to%20compare" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "firstText": "Text to compare against the second input",
  "secondText": "Second text to compare"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/winstonAI/latest/actions/compare-text?${params}`, {
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
| `firstText` | string | yes | The first text to compare. Example: `Text to compare against the second input`. |
| `secondText` | string | yes | The second text to compare. Example: `Second text to compare`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "credits_remaining": 1,
      "credits_used": 1,
      "first_text": {},
      "second_text": {},
      "similarity_score": 1,
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `credits_remaining` | number | Remaining Winston AI credits after the request. |
| `credits_used` | number | Credits consumed by the comparison request. |
| `first_text` | object | Similarity details for the first text. |
| `second_text` | object | Similarity details for the second text. |
| `similarity_score` | number | Overall similarity score between the two texts. |
| `status` | number | HTTP status code returned by Winston AI. |

## Native endpoint

Through the native Winston AI API, this operation is `POST /v2/text-compare` (base URL `https://api.gowinston.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/compare-text.md) for the provider-specific parameters and requirements.

