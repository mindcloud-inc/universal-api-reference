# Orshot Universal API Examples

These examples use the MindCloud API key and Orshot connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Profile and Workspaces



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/orshot/latest/actions/get-profile-and-workspaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/orshot/latest/actions/get-profile-and-workspaces?${params}`, {
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
      "email": "ava@example.com",
      "name": "Ava Chen",
      "user_id": "string",
      "workspaces": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Get Profile and Workspaces action reference](actions/get-profile-and-workspaces.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/orshot/latest/actions/get-profile-and-workspaces).

## Add Brand Color



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/orshot/latest/actions/add-brand-color" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "value": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/orshot/latest/actions/add-brand-color', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "value": "string"
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
      "id": 1,
      "tags": [
        "string"
      ],
      "type": "string",
      "userId": "string",
      "value": "string",
      "workspaceId": 1
    }
  ],
  "meta": {}
}
```

See the full [Add Brand Color action reference](actions/add-brand-color.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/orshot/latest/actions/add-brand-color).
