# SafetyCulture: Get Inspection Answers

Retrieves inspection answers from SafetyCulture.

```
GET https://connect.mindcloud.co/v1/universal/safetyCulture/latest/actions/get-inspection-answers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SafetyCulture `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/safetyCulture/latest/actions/get-inspection-answers?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/safetyCulture/latest/actions/get-inspection-answers?${params}`, {
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
| `id` | string | yes | The unique identifier for the inspection |

## Response

```json
{
  "success": true,
  "data": [
    {
      "datetimeAnswer": {
        "answer": "2026-05-07T12:00:00.000Z"
      },
      "modifiedAt": "2026-05-07T12:00:00.000Z",
      "questionId": "string",
      "siteAnswer": {
        "name": "Ava Chen"
      },
      "temperatureAnswer": {
        "answer": 1
      },
      "textAnswer": {
        "answer": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `datetimeAnswer.answer` | date |  |
| `modifiedAt` | date |  |
| `questionId` | string |  |
| `siteAnswer.name` | string |  |
| `temperatureAnswer.answer` | number |  |
| `textAnswer.answer` | string |  |

## Native endpoint

Through the native SafetyCulture API, this operation is `GET /inspections/v1/answers/{id}` (base URL `https://api.safetyculture.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-inspection-answers.md) for the provider-specific parameters and requirements.

