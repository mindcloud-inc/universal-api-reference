# Journy.io Universal API Examples

These examples use the MindCloud API key and Journy.io connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Validate API Key



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/journyio/latest/actions/validate-api-key?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/journyio/latest/actions/validate-api-key?${params}`, {
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
      "permissions": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

See the full [Validate API Key action reference](actions/validate-api-key.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/journyio/latest/actions/validate-api-key).

## Add Users to Account



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/journyio/latest/actions/add-users-to-account" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "users[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/journyio/latest/actions/add-users-to-account', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "users[]": [{}]
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
      "message": "string",
      "meta": {
        "requestId": "string",
        "status": 1
      }
    }
  ],
  "meta": {}
}
```

See the full [Add Users to Account action reference](actions/add-users-to-account.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/journyio/latest/actions/add-users-to-account).
