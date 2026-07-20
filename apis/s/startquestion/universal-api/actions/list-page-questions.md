# Startquestion: List Page Questions

Retrieves questions for a Startquestion survey page.

```
GET https://connect.mindcloud.co/v1/universal/startquestion/latest/actions/list-page-questions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Startquestion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/startquestion/latest/actions/list-page-questions?connectionId=$CONNECTION_ID&surveyId=1&pageId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "surveyId": "1",
  "pageId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/startquestion/latest/actions/list-page-questions?${params}`, {
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
| `id` | string | no | Probe arg. |
| `surveyId` | number | yes | Survey ID. |
| `pageId` | number | yes | Page ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "answers": [
        {}
      ],
      "answers_count": 1,
      "desc": "string",
      "id": 1,
      "id_page": 1,
      "internalName": "Ava Chen",
      "number": 1,
      "options": {},
      "required": 1,
      "scales": [
        {}
      ],
      "text": "string",
      "type": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `answers` | array<object> | Answer options. |
| `answers_count` | number | Answer option count. |
| `desc` | string | Question description. |
| `id` | number | Question ID. |
| `id_page` | number | Page ID. |
| `internalName` | string | Internal name. |
| `number` | number | Question order. |
| `options` | object | Question options. |
| `required` | number | Required flag. |
| `scales` | array<object> | Scale options. |
| `text` | string | Question text. |
| `type` | number | Question type code. |

## Native endpoint

Through the native Startquestion API, this operation is `GET /questions/:id_survey/:id_page` (base URL `https://www.startquestion.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-page-questions.md) for the provider-specific parameters and requirements.

