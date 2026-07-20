# Cognito Forms Universal API Examples

These examples use the MindCloud API key and Cognito Forms connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Forms



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cognitoForms/latest/actions/list-forms?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cognitoForms/latest/actions/list-forms?${params}`, {
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
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [List Forms action reference](actions/list-forms.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cognitoForms/latest/actions/list-forms).

## Create Entry



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cognitoForms/latest/actions/create-entry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "formId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cognitoForms/latest/actions/create-entry', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "formId": "string"
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
      "entry": {
        "action": "string",
        "dateCreated": "2026-05-07T12:00:00.000Z",
        "dateUpdated": "2026-05-07T12:00:00.000Z",
        "role": "string",
        "status": "string"
      },
      "id": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Entry action reference](actions/create-entry.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cognitoForms/latest/actions/create-entry).
