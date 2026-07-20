# Google Forms: Create Choice Question

Creates a choice question in Google Forms.

```
PUT https://connect.mindcloud.co/v1/universal/googleForms/latest/actions/create-choice-question
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Forms `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/googleForms/latest/actions/create-choice-question" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "formId": "string",
  "title": "string",
  "locationIndex": 1,
  "choiceType": "0",
  "options[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleForms/latest/actions/create-choice-question', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "formId": "string",
    "title": "string",
    "locationIndex": 1,
    "choiceType": "0",
    "options[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `formId` | string | yes | The form identifier. |
| `title` | string | yes | Question text shown to respondents. |
| `description` | string | no | Optional help text displayed below the question title. |
| `locationIndex` | number | yes | Where to place the new item in the form. |
| `required` | boolean | no | Require respondents to answer this question. |
| `choiceType` | list | yes | Choice question type: radio buttons, checkboxes, or dropdown. One of: `0`, `1`, `2`. |
| `options[]` | array<string> | yes | Choices shown to respondents. Accepts multiple values as an array. |
| `shuffle` | boolean | no | Randomize options for each respondent. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `pointValue` | number | no | Quiz point value for this question. |
| `correctAnswers[]` | array<string> | no | Choice values that are correct for quiz grading. Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "writeControl": {
        "requiredRevisionId": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `writeControl.requiredRevisionId` | string |  |

## Native endpoint

Through the native Google Forms API, this operation is `POST /:formId:batchUpdate` (base URL `https://forms.googleapis.com/v1/forms`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-choice-question.md) for the provider-specific parameters and requirements.

