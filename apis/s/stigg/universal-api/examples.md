# Stigg Universal API Examples

These examples use the MindCloud API key and Stigg connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## API Key Scope



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stigg/latest/actions/api-key-scope?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stigg/latest/actions/api-key-scope?${params}`, {
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
      "displayName": "Ava Chen",
      "id": "string",
      "items": [
        {}
      ],
      "message": "string",
      "name": "Ava Chen",
      "refId": "string",
      "status": "string",
      "success": true,
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [API Key Scope action reference](actions/api-key-scope.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/stigg/latest/actions/api-key-scope).

## Create One Addon



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/stigg/latest/actions/create-one-addon" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/stigg/latest/actions/create-one-addon', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
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
      "id": "string",
      "items": [
        {}
      ],
      "message": "string",
      "refId": "string",
      "status": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Create One Addon action reference](actions/create-one-addon.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/stigg/latest/actions/create-one-addon).
