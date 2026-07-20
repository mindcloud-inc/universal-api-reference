# Loopy Loyalty Universal API Examples

These examples use the MindCloud API key and Loopy Loyalty connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Stamp Images



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/list-stamp-images?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/list-stamp-images?${params}`, {
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
  "data": [],
  "meta": {}
}
```

See the full [List Stamp Images action reference](actions/list-stamp-images.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/loopyLoyalty/latest/actions/list-stamp-images).

## Add Stamps By Card ID



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/add-stamps-by-card-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "cid": "RDX5AsgKYa3UZ7",
  "stamps": "10"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/add-stamps-by-card-id', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "cid": "RDX5AsgKYa3UZ7",
    "stamps": "10"
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
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Add Stamps By Card ID action reference](actions/add-stamps-by-card-id.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/loopyLoyalty/latest/actions/add-stamps-by-card-id).
