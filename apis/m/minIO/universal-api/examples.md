# MinIO Universal API Examples

These examples use the MindCloud API key and MinIO connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Buckets



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/minIO/latest/actions/list-buckets?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/minIO/latest/actions/list-buckets?${params}`, {
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

See the full [List Buckets action reference](actions/list-buckets.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/minIO/latest/actions/list-buckets).

## Copy Object



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/minIO/latest/actions/copy-object" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/minIO/latest/actions/copy-object', {
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
  "data": [],
  "meta": {}
}
```

See the full [Copy Object action reference](actions/copy-object.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/minIO/latest/actions/copy-object).
