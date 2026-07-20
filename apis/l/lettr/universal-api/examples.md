# Lettr Universal API Examples

These examples use the MindCloud API key and Lettr connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Auth Check



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lettr/latest/actions/auth-check?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lettr/latest/actions/auth-check?${params}`, {
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
      "data": {
        "team_id": 1,
        "timestamp": "2026-05-07T12:00:00.000Z"
      },
      "message": "string"
    }
  ],
  "meta": {}
}
```

See the full [Auth Check action reference](actions/auth-check.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/lettr/latest/actions/auth-check).

## Create Domain



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/lettr/latest/actions/create-domain" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "domain": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lettr/latest/actions/create-domain', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "domain": "string"
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
        "dkim": {
          "headers": "string",
          "public": "string",
          "selector": "string",
          "signing_domain": "string"
        },
        "domain": "string",
        "status": "string",
        "status_label": "string"
      },
      "message": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Domain action reference](actions/create-domain.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/lettr/latest/actions/create-domain).
