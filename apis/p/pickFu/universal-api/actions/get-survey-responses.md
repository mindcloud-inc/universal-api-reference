# PickFu: Get Survey Responses



```
GET https://connect.mindcloud.co/v1/universal/pickFu/latest/actions/get-survey-responses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PickFu `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pickFu/latest/actions/get-survey-responses?connectionId=$CONNECTION_ID&limit=25&offset=0&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pickFu/latest/actions/get-survey-responses?${params}`, {
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
| `id` | string | yes | Survey GUID. |
| `questionId` | string | no | Filter responses to a specific question GUID. |
| `language` | string | no | Language code for response translations. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "chosen_option": "string",
      "clicks": [
        {}
      ],
      "explanation": "string",
      "id": "string",
      "matchup": {},
      "media": "string",
      "media_transcription": "string",
      "question_id": "string",
      "respondent": [
        {}
      ],
      "rounds": [
        {}
      ],
      "score": 1,
      "translation": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `chosen_option` | string | Label of the chosen option. |
| `clicks` | array<object> | Click coordinates for click-test questions. |
| `explanation` | string | Written explanation from the respondent. |
| `id` | string | Response ID. |
| `matchup` | object | Head-to-head matchup pairing shown to the respondent. |
| `media` | string | Media URL for screen-recording style responses. |
| `media_transcription` | string | Transcription of recorded media. |
| `question_id` | string | Question GUID for multi-question surveys. |
| `respondent` | array<object> | Respondent demographic traits. |
| `rounds` | array<object> | Tournament rounds for ranked question types. |
| `score` | number | Rating score for rating-style questions. |
| `translation` | string | Translated explanation text. |

## Native endpoint

Through the native PickFu API, this operation is `GET /surveys/[:id]/responses` (base URL `https://api.pickfu.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-survey-responses.md) for the provider-specific parameters and requirements.

