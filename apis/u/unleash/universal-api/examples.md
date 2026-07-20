# Unleash Universal API Examples

These examples use the MindCloud API key and Unleash connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get projects

Retrieves projects from Unleash.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/unleash/latest/actions/get-projects?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/unleash/latest/actions/get-projects?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "defaultStickiness": "string",
      "description": "string",
      "featureCount": 1,
      "health": 1,
      "id": "string",
      "memberCount": 1,
      "mode": "string",
      "name": "Ava Chen",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Get projects action reference](actions/get-projects.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/unleash/latest/actions/get-projects).

## Configure Project Access

Configures project access in Unleash.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/unleash/latest/actions/addaccesstoproject" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "body": {},
  "projectId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/unleash/latest/actions/addaccesstoproject', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "body": {},
    "projectId": "string"
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": "string",
      "message": "string",
      "name": "Ava Chen",
      "success": true,
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Configure Project Access action reference](actions/addaccesstoproject.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/unleash/latest/actions/addaccesstoproject).
