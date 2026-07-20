# Convex Universal API Examples

These examples use the MindCloud API key and Convex connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Token Details

Retrieves details about the current Convex token.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/convex/latest/actions/get-token-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/convex/latest/actions/get-token-details?${params}`, {
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
      "createTime": 1,
      "name": "Ava Chen",
      "teamId": 1,
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Token Details action reference](actions/get-token-details.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/convex/latest/actions/get-token-details).

## Create Deployment

Creates a new deployment in Convex.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/convex/latest/actions/create-deployment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": 1,
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/convex/latest/actions/create-deployment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": 1,
    "type": "string"
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
      "class": "string",
      "createTime": 1,
      "creator": 1,
      "dashboardEditConfirmation": "string",
      "deploymentType": "string",
      "deploymentUrl": "https://example.com",
      "id": 1,
      "isDefault": true,
      "kind": "string",
      "name": "Ava Chen",
      "previewIdentifier": "string",
      "projectId": 1,
      "reference": "string",
      "region": "string",
      "sendLogsToClient": true
    }
  ],
  "meta": {}
}
```

See the full [Create Deployment action reference](actions/create-deployment.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/convex/latest/actions/create-deployment).
