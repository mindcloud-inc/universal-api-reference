# Instatus Universal API Examples

These examples use the MindCloud API key and Instatus connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get User Profile



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instatus/latest/actions/get-user-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instatus/latest/actions/get-user-profile?${params}`, {
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
      "email": "ava@example.com",
      "id": "string",
      "name": "Ava Chen",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Get User Profile action reference](actions/get-user-profile.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/instatus/latest/actions/get-user-profile).

## Create Component



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/instatus/latest/actions/create-component" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "pageId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/instatus/latest/actions/create-component', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "pageId": "string"
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
      "archivedAt": "2026-05-07T12:00:00.000Z",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "descriptionHtml": "string",
      "id": "string",
      "incidents": [
        {}
      ],
      "internalStatus": "string",
      "isCollapsed": true,
      "isParent": true,
      "name": "Ava Chen",
      "nameHtml": "Ava Chen",
      "order": 1,
      "showUptime": true,
      "siteId": "string",
      "status": "string",
      "translations": {},
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Create Component action reference](actions/create-component.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/instatus/latest/actions/create-component).
