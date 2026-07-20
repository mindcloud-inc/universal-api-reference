# Informizely: List Questions



```
GET https://connect.mindcloud.co/v1/universal/informizely/latest/actions/list-questions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Informizely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/informizely/latest/actions/list-questions?connectionId=$CONNECTION_ID&surveyId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "surveyId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/informizely/latest/actions/list-questions?${params}`, {
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
| `surveyId` | string | yes | The ID of the survey whose questions you want to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Choices": [
        {}
      ],
      "Id": "string",
      "Removed": true,
      "Text": "string",
      "Type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Choices` | array<object> | The available answer choices when the question type supports them. |
| `Id` | string | The question ID within the survey. |
| `Removed` | boolean | Whether the question was removed from the current survey. |
| `Text` | string | The question text. |
| `Type` | string | The Informizely question type. |

## Native endpoint

Through the native Informizely API, this operation is `GET /questions` (base URL `https://api.informizely.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-questions.md) for the provider-specific parameters and requirements.

