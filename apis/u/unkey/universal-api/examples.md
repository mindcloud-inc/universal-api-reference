# Unkey Universal API Examples

These examples use the MindCloud API key and Unkey connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Roles

Retrieves all configured roles from Unkey.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/unkey/latest/actions/list-roles?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/unkey/latest/actions/list-roles?${params}`, {
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
        [
          {}
        ]
      ],
      "meta": {
        "requestId": "string"
      },
      "pagination": {
        "cursor": "string",
        "hasMore": true
      }
    }
  ],
  "meta": {}
}
```

See the full [List Roles action reference](actions/list-roles.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/unkey/latest/actions/list-roles).

## Add key permissions

Adds permissions to an existing API key in Unkey.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/unkey/latest/actions/add-key-permissions" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "keyId": "string",
  "permissions[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/unkey/latest/actions/add-key-permissions', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "keyId": "string",
    "permissions[]": ["string"]
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
      "data": [
        [
          {}
        ]
      ],
      "meta": {
        "requestId": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [Add key permissions action reference](actions/add-key-permissions.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/unkey/latest/actions/add-key-permissions).
