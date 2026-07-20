# Google Forms Universal API Examples

These examples use the MindCloud API key and Google Forms connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Form

Retrieves a form from Google Forms.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleForms/latest/actions/get-form?connectionId=$CONNECTION_ID&formId=1FAIpQLSdExampleFormId" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "formId": "1FAIpQLSdExampleFormId"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleForms/latest/actions/get-form?${params}`, {
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
      "formId": "string",
      "info": {
        "documentTitle": "string",
        "title": "string"
      },
      "publishSettings": {
        "publishState": {
          "isAcceptingResponses": true,
          "isPublished": true
        }
      },
      "responderUri": "string",
      "revisionId": "string",
      "settings": {
        "emailCollectionType": "ava@example.com"
      }
    }
  ],
  "meta": {}
}
```

See the full [Get Form action reference](actions/get-form.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/googleForms/latest/actions/get-form).

## Add Questions To Form

Adds multiple questions to a form in Google Forms.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/googleForms/latest/actions/add-questions-to-form" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "formId": "string",
  "questions[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleForms/latest/actions/add-questions-to-form', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "formId": "string",
    "questions[]": [{}]
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

See the full [Add Questions To Form action reference](actions/add-questions-to-form.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/googleForms/latest/actions/add-questions-to-form).
