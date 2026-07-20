# DataForms.io Universal API Examples

These examples use the MindCloud API key and DataForms.io connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User

Retrieves the current user from DataForms.io.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dataFormsio/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dataFormsio/latest/actions/get-current-user?${params}`, {
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
      "data": {
        "companyId": "string",
        "createdAt": "string",
        "email": "ava@example.com",
        "firstname": "Ava",
        "id": "string",
        "lastname": "Chen",
        "locale": "string",
        "roleId": "string",
        "updatedAt": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [Get Current User action reference](actions/get-current-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dataFormsio/latest/actions/get-current-user).

## Create Data Form

Creates a new data form in DataForms.io.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dataFormsio/latest/actions/create-data-form" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "templateId": "string",
  "headline": "string",
  "type": "0"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dataFormsio/latest/actions/create-data-form', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "templateId": "string",
    "headline": "string",
    "type": "0"
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
      "data": {
        "allowMultipleSubmissions": true,
        "createdAt": "string",
        "headline": "string",
        "id": "string",
        "lockAfterSubmission": true,
        "redirectUrl": "https://example.com",
        "templateId": "string",
        "type": "string",
        "updatedAt": "string",
        "url": "https://example.com"
      }
    }
  ],
  "meta": {}
}
```

See the full [Create Data Form action reference](actions/create-data-form.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dataFormsio/latest/actions/create-data-form).
