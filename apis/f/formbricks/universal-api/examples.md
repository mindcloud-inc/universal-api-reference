# Formbricks Universal API Examples

These examples use the MindCloud API key and Formbricks connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Me

Retrieves the current user from Formbricks.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/formbricks/latest/actions/get-me?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/formbricks/latest/actions/get-me?${params}`, {
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
      "environments": [
        {
          "environmentId": "string",
          "environmentType": "string",
          "permission": "string",
          "projectId": "string",
          "projectName": "Ava Chen"
        }
      ],
      "organizationAccess": {
        "accessControl": {
          "read": true,
          "write": true
        }
      },
      "organizationId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Me action reference](actions/get-me.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/formbricks/latest/actions/get-me).

## Create Client Response

Creates a new client response in Formbricks.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/formbricks/latest/actions/create-client-response" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "environmentId": "string",
  "surveyId": "string",
  "finished": true,
  "data": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/formbricks/latest/actions/create-client-response', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "environmentId": "string",
    "surveyId": "string",
    "finished": true,
    "data": {}
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
        "id": "string",
        "quotaFull": true
      }
    }
  ],
  "meta": {}
}
```

See the full [Create Client Response action reference](actions/create-client-response.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/formbricks/latest/actions/create-client-response).
