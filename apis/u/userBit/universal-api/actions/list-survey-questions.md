# UserBit: List Survey Questions

Retrieves survey questions from a UserBit survey.

```
GET https://connect.mindcloud.co/v1/universal/userBit/latest/actions/list-survey-questions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UserBit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/userBit/latest/actions/list-survey-questions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/userBit/latest/actions/list-survey-questions?${params}`, {
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
      "content": "string",
      "id": "string",
      "order": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | string | Question content. |
| `id` | string | Survey question identifier. |
| `order` | number | Question order in the survey. |

## Native endpoint

Through the native UserBit API, this operation is `GET /v1/surveys/questions/list` (base URL `https://userbit.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-survey-questions.md) for the provider-specific parameters and requirements.

