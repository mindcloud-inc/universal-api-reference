# Shadify: Generate Capital Quiz

Retrieves a capital quiz from Shadify.

```
GET https://connect.mindcloud.co/v1/universal/shadify/latest/actions/generate-capital-quiz
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shadify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shadify/latest/actions/generate-capital-quiz?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shadify/latest/actions/generate-capital-quiz?${params}`, {
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
| `variants` | number | no | Optional number of answer variants from 2 to 6. Default is 4. Default: `4`. |
| `amount` | number | no | Optional number of unique quizzes from 1 to 20. Default is 1. Default: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "answer": "string",
      "country": "string",
      "flag": "string",
      "variants": [
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
| `answer` | string | Correct capital answer. |
| `country` | string | Country to guess the capital for. |
| `flag` | string | Flag image URL. |
| `variants` | array<string> | Answer variants. |

## Native endpoint

Through the native Shadify API, this operation is `GET /countries/capital-quiz` (base URL `https://shadify.yurace.pro/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-capital-quiz.md) for the provider-specific parameters and requirements.

