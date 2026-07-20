# mintBlue Universal API Examples

These examples use the MindCloud API key and mintBlue connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Projects

Retrieves projects from mintBlue.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mintBlue/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mintBlue/latest/actions/list-projects?${params}`, {
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
      "archived_at": "string",
      "avg_transactions_size": 1,
      "created_at": "string",
      "default_key_id": "string",
      "description": "string",
      "id": "string",
      "name": "Ava Chen",
      "tags": [
        "string"
      ],
      "total_transactions_count": 1,
      "total_transactions_size": 1
    }
  ],
  "meta": {}
}
```

See the full [List Projects action reference](actions/list-projects.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mintBlue/latest/actions/list-projects).

## Create Access Token

Creates a new access token in mintBlue.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mintBlue/latest/actions/create-access-token" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "params.name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mintBlue/latest/actions/create-access-token', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "params.name": "Ava Chen"
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
      "apiToken": "string",
      "sdkToken": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Access Token action reference](actions/create-access-token.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mintBlue/latest/actions/create-access-token).
