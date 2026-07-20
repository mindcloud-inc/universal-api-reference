# Release0 Universal API Examples

These examples use the MindCloud API key and Release0 connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Workspaces

Retrieves workspaces the current user can access in Release0.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/release0/latest/actions/list-workspaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/release0/latest/actions/list-workspaces?${params}`, {
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
      "icon": "string",
      "id": "string",
      "name": "Ava Chen",
      "plan": "string",
      "slug": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Workspaces action reference](actions/list-workspaces.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/release0/latest/actions/list-workspaces).

## Create Agent

Creates a new agent in Release0.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/release0/latest/actions/create-agent" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/release0/latest/actions/create-agent', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceId": "string"
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
      "exposure": {
        "access": {
          "url": "https://example.com"
        },
        "state": {
          "published": true
        }
      },
      "profile": {
        "title": "string"
      },
      "ref": {
        "key": "string",
        "publicKey": "string",
        "revision": "string"
      },
      "tenancy": {
        "workspaceRef": "string"
      },
      "timestamps": {
        "created": "string",
        "updated": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [Create Agent action reference](actions/create-agent.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/release0/latest/actions/create-agent).
