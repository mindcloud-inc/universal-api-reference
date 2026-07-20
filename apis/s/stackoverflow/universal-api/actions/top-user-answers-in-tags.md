# Stackoverflow: List Top Answers In Tags By User

Retrieves a user's top answers in tags from Stackoverflow.

```
GET https://connect.mindcloud.co/v1/universal/stackoverflow/latest/actions/top-user-answers-in-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stackoverflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stackoverflow/latest/actions/top-user-answers-in-tags?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stackoverflow/latest/actions/top-user-answers-in-tags?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "answer_id": 1,
      "is_accepted": true,
      "question_id": 1,
      "score": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `answer_id` | number |  |
| `is_accepted` | boolean |  |
| `question_id` | number |  |
| `score` | number |  |

## Native endpoint

Through the native Stackoverflow API, this operation is `GET /users/[:id]/tags/[:tags]/top-answers` (base URL `https://api.stackexchange.com/2.3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/top-user-answers-in-tags.md) for the provider-specific parameters and requirements.

