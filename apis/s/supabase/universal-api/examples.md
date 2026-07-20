# Supabase Universal API Examples

These examples use the MindCloud API key and Supabase connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Buckets

Retrieves storage buckets from your Supabase project.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/supabase/latest/actions/list-buckets?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/supabase/latest/actions/list-buckets?${params}`, {
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
      "allowedMimeTypes": [
        "string"
      ],
      "createdAt": "2026-05-07T12:00:00.000Z",
      "fileSizeLimit": 1,
      "id": "string",
      "name": "Ava Chen",
      "owner": "string",
      "public": true,
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [List Buckets action reference](actions/list-buckets.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/supabase/latest/actions/list-buckets).

## Copy Object

Copies an object between paths in Supabase storage.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/supabase/latest/actions/copy-object" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/supabase/latest/actions/copy-object', {
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
      "bucketId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "key": "string",
      "lastAccessedAt": "2026-05-07T12:00:00.000Z",
      "metadata": {},
      "name": "Ava Chen",
      "owner": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "userMetadata": {},
      "version": "string"
    }
  ],
  "meta": {}
}
```

See the full [Copy Object action reference](actions/copy-object.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/supabase/latest/actions/copy-object).
