# Optform: Update Long Text Question

Updates an existing long-text question in an Optform form.

```
PUT https://connect.mindcloud.co/v1/universal/optform/latest/actions/update-long-text-question
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Optform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/optform/latest/actions/update-long-text-question" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "sortOrder": "1",
  "formId": "string",
  "userId": "string",
  "title": "string",
  "question": "string",
  "content": "string",
  "_etag": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/optform/latest/actions/update-long-text-question', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "sortOrder": "1",
    "formId": "string",
    "userId": "string",
    "title": "string",
    "question": "string",
    "content": "string",
    "_etag": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes |  |
| `sortOrder` | number | yes | Default: `1`. |
| `formId` | string | yes |  |
| `userId` | string | yes |  |
| `title` | string | yes |  |
| `question` | string | yes |  |
| `content` | string | yes |  |
| `_etag` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accept": "string",
      "allowOther": "string",
      "answer": "string",
      "answered": "string",
      "calculatorConfig": "string",
      "case": "string",
      "className": "Ava Chen",
      "columns": [
        "string"
      ],
      "content": "string",
      "description": "string",
      "descriptionLink": [
        "https://example.com"
      ],
      "Etag": "string",
      "formId": "string",
      "helpText": "string",
      "helpTextShow": "string",
      "html": "string",
      "id": "string",
      "index": "string",
      "inline": "string",
      "jump": "string",
      "jumpLogic": {},
      "labelLeft": "string",
      "labelRight": "string",
      "links": [
        "https://example.com"
      ],
      "mask": "string",
      "max": "string",
      "maxLength": "string",
      "maxSize": "string",
      "min": "string",
      "multiple": "string",
      "nextStepOnAnswer": "string",
      "options": [
        "string"
      ],
      "other": "string",
      "placeholder": "string",
      "required": "string",
      "rows": [
        "string"
      ],
      "sortOrder": 1,
      "subtitle": "string",
      "tagline": "string",
      "title": "string",
      "type": "string",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accept` | string |  |
| `allowOther` | string |  |
| `answer` | string |  |
| `answered` | string |  |
| `calculatorConfig` | string |  |
| `case` | string |  |
| `className` | string |  |
| `columns` | array<string> |  |
| `content` | string |  |
| `description` | string |  |
| `descriptionLink` | array<string> |  |
| `Etag` | string |  |
| `formId` | string |  |
| `helpText` | string |  |
| `helpTextShow` | string |  |
| `html` | string |  |
| `id` | string |  |
| `index` | string |  |
| `inline` | string |  |
| `jump` | string |  |
| `jumpLogic` | object |  |
| `labelLeft` | string |  |
| `labelRight` | string |  |
| `links` | array<string> |  |
| `mask` | string |  |
| `max` | string |  |
| `maxLength` | string |  |
| `maxSize` | string |  |
| `min` | string |  |
| `multiple` | string |  |
| `nextStepOnAnswer` | string |  |
| `options` | array<string> |  |
| `other` | string |  |
| `placeholder` | string |  |
| `required` | string |  |
| `rows` | array<string> |  |
| `sortOrder` | number |  |
| `subtitle` | string |  |
| `tagline` | string |  |
| `title` | string |  |
| `type` | string |  |
| `userId` | string |  |

## Native endpoint

Through the native Optform API, this operation is `PUT /api/Form/questions` (base URL `https://optform.azure-api.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-long-text-question.md) for the provider-specific parameters and requirements.

