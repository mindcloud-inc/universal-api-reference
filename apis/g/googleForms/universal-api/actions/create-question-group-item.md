# Google Forms: Create Question Group Item

Creates a question group item in Google Forms.

```
PUT https://connect.mindcloud.co/v1/universal/googleForms/latest/actions/create-question-group-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Forms `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/googleForms/latest/actions/create-question-group-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "formId": "string",
  "title": "string",
  "locationIndex": 1,
  "rows[]": [
    "string"
  ],
  "columns[]": [
    "string"
  ],
  "choiceType": "0"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleForms/latest/actions/create-question-group-item', {
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
    "rows[]": ["string"],
    "columns[]": ["string"],
    "choiceType": "0"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `formId` | string | yes | The form identifier. |
| `title` | string | yes | Question group title. |
| `description` | string | no | Optional help text displayed below the group title. |
| `locationIndex` | number | yes | Where to place the new question group in the form. |
| `rows[]` | array<string> | yes | Row question labels. Accepts multiple values as an array. |
| `columns[]` | array<string> | yes | Shared choice labels for each row. Accepts multiple values as an array. |
| `choiceType` | list | yes | Grid choice type. Google supports radio or checkbox for grids. One of: `0`, `1`. |
| `shuffleQuestions` | boolean | no | Randomize row order for respondents. |

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

Through the native Google Forms API, this operation is `POST /:formId:batchUpdate` (base URL `https://forms.googleapis.com/v1/forms`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-question-group-item.md) for the provider-specific parameters and requirements.

