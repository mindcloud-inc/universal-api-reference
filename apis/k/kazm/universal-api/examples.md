# Kazm Universal API Examples

These examples use the MindCloud API key and Kazm connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Organization Balance

Retrieves the organization balance from Kazm.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kazm/latest/actions/get-organization-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kazm/latest/actions/get-organization-balance?${params}`, {
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
      "balance_dollars": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Organization Balance action reference](actions/get-organization-balance.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/kazm/latest/actions/get-organization-balance).

## Add File To Set

Adds a file to a Kazm file set.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/kazm/latest/actions/add-file-to-set" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kazm/latest/actions/add-file-to-set', {
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
      "original_file_name": "Ava Chen",
      "retry_count": 1,
      "size_bytes": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add File To Set action reference](actions/add-file-to-set.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/kazm/latest/actions/add-file-to-set).
