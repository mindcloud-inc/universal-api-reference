# Optform Universal API Examples

These examples use the MindCloud API key and Optform connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Form Responses

Retrieves form responses from Optform.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/optform/latest/actions/list-form-responses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/optform/latest/actions/list-form-responses?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "answers": [
        {}
      ],
      "count": 1,
      "formId": "string",
      "id": 1
    }
  ],
  "meta": {}
}
```

See the full [List Form Responses action reference](actions/list-form-responses.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/optform/latest/actions/list-form-responses).

## Add Long Text Question

Creates a new long-text question in an Optform form.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/optform/latest/actions/add-long-text-question" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "1",
  "sortOrder": "1",
  "formId": "string",
  "userId": "string",
  "title": "string",
  "question": "string",
  "content": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/optform/latest/actions/add-long-text-question', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "1",
    "sortOrder": "1",
    "formId": "string",
    "userId": "string",
    "title": "string",
    "question": "string",
    "content": "string"
  })
});

const { success, data } = await response.json();
```

Example response:

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

See the full [Add Long Text Question action reference](actions/add-long-text-question.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/optform/latest/actions/add-long-text-question).
