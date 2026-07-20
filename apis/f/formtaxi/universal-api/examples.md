# Form.taxi Universal API Examples

These examples use the MindCloud API key and Form.taxi connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Form Submissions

Retrieves form submissions from Form.taxi.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/formtaxi/latest/actions/list-form-submissions?connectionId=$CONNECTION_ID&limit=25&offset=0&formCode=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "formCode": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/formtaxi/latest/actions/list-form-submissions?${params}`, {
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
      "_box": "string",
      "_date": "2026-05-07T12:00:00.000Z",
      "_id": "string",
      "_url": "https://example.com",
      "attachments": [
        {}
      ],
      "fields": {},
      "fields_summary": {
        "html": "string",
        "markdown": "string",
        "text": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [List Form Submissions action reference](actions/list-form-submissions.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/formtaxi/latest/actions/list-form-submissions).

## Create Endpoint

Creates a new endpoint in Form.taxi.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/formtaxi/latest/actions/create-endpoint" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "user@example.com",
  "formName": "Contact Form",
  "language": "en"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/formtaxi/latest/actions/create-endpoint', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "user@example.com",
    "formName": "Contact Form",
    "language": "en"
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
      "endpoint_url": "https://example.com",
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Create Endpoint action reference](actions/create-endpoint.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/formtaxi/latest/actions/create-endpoint).
