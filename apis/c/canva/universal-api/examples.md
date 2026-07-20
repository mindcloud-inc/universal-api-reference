# Canva Universal API Examples

These examples use the MindCloud API key and Canva connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User

Retrieves details for the current Canva user.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/canva/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/canva/latest/actions/get-current-user?${params}`, {
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
      "teamUser": {
        "teamId": "string",
        "userId": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [Get Current User action reference](actions/get-current-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/canva/latest/actions/get-current-user).

## Create Design

Creates a new design in Canva.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/canva/latest/actions/create-design" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "designType.type": "custom"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/canva/latest/actions/create-design', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "designType.type": "custom"
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
      "design": {
        "createdAt": 1,
        "id": "string",
        "owner": {
          "teamId": "string",
          "userId": "string"
        },
        "pageCount": 1,
        "title": "string",
        "updatedAt": 1,
        "urls": {
          "editUrl": "https://example.com",
          "viewUrl": "https://example.com"
        }
      }
    }
  ],
  "meta": {}
}
```

See the full [Create Design action reference](actions/create-design.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/canva/latest/actions/create-design).
