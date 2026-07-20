# Google Forms: Create Rating Question

Creates a rating question in Google Forms.

```
PUT https://connect.mindcloud.co/v1/universal/googleForms/latest/actions/create-rating-question
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Forms `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/googleForms/latest/actions/create-rating-question" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "formId": "string",
  "title": "string",
  "locationIndex": 1,
  "ratingScaleLevel": 1,
  "iconType": "STAR"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleForms/latest/actions/create-rating-question', {
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
    "ratingScaleLevel": 1,
    "iconType": "STAR"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `formId` | string | yes | The form identifier. |
| `title` | string | yes | Question title shown to respondents. |
| `description` | string | no | Optional help text shown under the title. |
| `locationIndex` | number | yes | Index where the question should be inserted. |
| `required` | boolean | no | Whether respondents must answer this question. |
| `ratingScaleLevel` | number | yes | Number of rating icons to show. |
| `iconType` | list | yes | Icon used for the rating scale. Default: `STAR`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `includeFormInResponse` | boolean | no | Return the updated form in the response. |
| `requiredRevisionId` | string | no | Only apply the update if the form is still at this revision. |
| `targetRevisionId` | string | no | Apply this update against a recent revision and let Google transform non-conflicting changes. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "formId": "string",
      "replies": [
        [
          {}
        ]
      ],
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
| `formId` | string | ID of the updated form. |
| `replies[]` | array<object> | Batch update replies. Create-item replies include the created item ID and question ID when returned. |
| `writeControl.requiredRevisionId` | string | Revision ID for subsequent guarded writes. |

## Native endpoint

Through the native Google Forms API, this operation is `POST /:formId:batchUpdate` (base URL `https://forms.googleapis.com/v1/forms`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-rating-question.md) for the provider-specific parameters and requirements.

