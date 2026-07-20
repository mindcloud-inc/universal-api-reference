# Google Cloud Storage Universal API Examples

These examples use the MindCloud API key and Google Cloud Storage connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Buckets

Retrieves a list of buckets from Google Cloud Storage.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleCloudStorage/latest/actions/list-buckets?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleCloudStorage/latest/actions/list-buckets?${params}`, {
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
      "id": "string",
      "location": "string",
      "metageneration": "string",
      "name": "Ava Chen",
      "selfLink": "https://example.com",
      "storageClass": "string",
      "timeCreated": "2026-05-07T12:00:00.000Z",
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [List Buckets action reference](actions/list-buckets.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/googleCloudStorage/latest/actions/list-buckets).

## Compose Object

Composes multiple objects into one in Google Cloud Storage.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/googleCloudStorage/latest/actions/compose-object" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "destinationBucket": "string",
  "destinationObject": "string",
  "sourceObjects[]": [
    {}
  ],
  "sourceObjects[].name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleCloudStorage/latest/actions/compose-object', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "destinationBucket": "string",
    "destinationObject": "string",
    "sourceObjects[]": [{}],
    "sourceObjects[].name": "Ava Chen"
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
      "bucket": "string",
      "componentCount": 1,
      "contentType": "string",
      "generation": "string",
      "id": "string",
      "name": "Ava Chen",
      "size": "string"
    }
  ],
  "meta": {}
}
```

See the full [Compose Object action reference](actions/compose-object.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/googleCloudStorage/latest/actions/compose-object).
