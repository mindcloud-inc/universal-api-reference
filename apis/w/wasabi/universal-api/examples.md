# Wasabi Universal API Examples

These examples use the MindCloud API key and Wasabi connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Buckets

Retrieves the buckets available in your Wasabi account.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wasabi/latest/actions/list-buckets?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wasabi/latest/actions/list-buckets?${params}`, {
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
      "bucketRegion": "string",
      "creationDate": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [List Buckets action reference](actions/list-buckets.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/wasabi/latest/actions/list-buckets).

## Create Bucket

Creates a new bucket in Wasabi.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/wasabi/latest/actions/create-bucket" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "mindcloud-wasabi-agent-20260422"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wasabi/latest/actions/create-bucket', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "mindcloud-wasabi-agent-20260422"
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
      "location": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Create Bucket action reference](actions/create-bucket.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/wasabi/latest/actions/create-bucket).
