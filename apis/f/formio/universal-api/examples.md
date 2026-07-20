# Form.io Universal API Examples

These examples use the MindCloud API key and Form.io connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Project

Retrieves details for your Form.io project.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/formio/latest/actions/get-project?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/formio/latest/actions/get-project?${params}`, {
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
      "_id": "string",
      "access": [
        {}
      ],
      "created": "string",
      "description": "string",
      "modified": "string",
      "name": "Ava Chen",
      "owner": "string",
      "plan": "string",
      "public": {},
      "settings": {},
      "stageTitle": "string",
      "tag": "string",
      "title": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Project action reference](actions/get-project.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/formio/latest/actions/get-project).

## Create Admin Submission

Creates a new admin submission in your Form.io project.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/formio/latest/actions/create-admin-submission" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "password": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/formio/latest/actions/create-admin-submission', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "password": "string"
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
      "_id": "string",
      "created": "string",
      "data": {},
      "form": "string",
      "modified": "string",
      "owner": "string",
      "project": "string",
      "state": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Admin Submission action reference](actions/create-admin-submission.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/formio/latest/actions/create-admin-submission).
