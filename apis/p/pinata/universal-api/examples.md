# Pinata Universal API Examples

These examples use the MindCloud API key and Pinata connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Test Authentication

Retrieves the current authentication status from Pinata.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pinata/latest/actions/test-authentication?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pinata/latest/actions/test-authentication?${params}`, {
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
      "message": "string"
    }
  ],
  "meta": {}
}
```

See the full [Test Authentication action reference](actions/test-authentication.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pinata/latest/actions/test-authentication).

## Add File To Group

Updates a Pinata group by adding a file.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pinata/latest/actions/add-file-to-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fileId": "string",
  "id": "string",
  "network": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pinata/latest/actions/add-file-to-group', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fileId": "string",
    "id": "string",
    "network": "string"
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
      "data": {}
    }
  ],
  "meta": {}
}
```

See the full [Add File To Group action reference](actions/add-file-to-group.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pinata/latest/actions/add-file-to-group).
