# Currents Universal API Examples

These examples use the MindCloud API key and Currents connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Projects



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/currents/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/currents/latest/actions/list-projects?${params}`, {
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
      "data": [
        {
          "createdAt": "string",
          "cursor": "string",
          "defaultBranchName": "Ava Chen",
          "failFast": true,
          "inactivityTimeoutSeconds": 1,
          "name": "Ava Chen",
          "projectId": "string"
        }
      ],
      "has_more": true,
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Projects action reference](actions/list-projects.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/currents/latest/actions/list-projects).

## Generate Test Signature



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/currents/latest/actions/generate-test-signature" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "string",
  "specFilePath": "string",
  "testTitle": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/currents/latest/actions/generate-test-signature', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "string",
    "specFilePath": "string",
    "testTitle": "string"
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
        "signature": "string"
      },
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Generate Test Signature action reference](actions/generate-test-signature.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/currents/latest/actions/generate-test-signature).
