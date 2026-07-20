# Stackoverflow: Delete Question

Deletes an existing question from Stackoverflow.

```
DELETE https://connect.mindcloud.co/v1/universal/stackoverflow/latest/actions/delete-question
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stackoverflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/stackoverflow/latest/actions/delete-question?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stackoverflow/latest/actions/delete-question?${params}`, {
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
      "link": "https://example.com",
      "question_id": 1,
      "score": 1,
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `link` | string |  |
| `question_id` | number |  |
| `score` | number |  |
| `title` | string |  |

## Native endpoint

Through the native Stackoverflow API, this operation is `POST /questions/[:id]/delete` (base URL `https://api.stackexchange.com/2.3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-question.md) for the provider-specific parameters and requirements.

