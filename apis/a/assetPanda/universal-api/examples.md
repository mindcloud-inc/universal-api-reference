# Asset Panda Universal API Examples

These examples use the MindCloud API key and Asset Panda connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Retrieve Self Details

Retrieves your user details from Asset Panda.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/assetPanda/latest/actions/retrieve-self-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/assetPanda/latest/actions/retrieve-self-details?${params}`, {
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

See the full [Retrieve Self Details action reference](actions/retrieve-self-details.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/assetPanda/latest/actions/retrieve-self-details).

## Archive Objects

Archives objects in Asset Panda.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/assetPanda/latest/actions/archive-objects" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/assetPanda/latest/actions/archive-objects', {
  method: 'PUT',
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
  "data": [],
  "meta": {}
}
```

See the full [Archive Objects action reference](actions/archive-objects.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/assetPanda/latest/actions/archive-objects).
