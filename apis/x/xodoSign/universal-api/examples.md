# Xodo Sign Universal API Examples

These examples use the MindCloud API key and Xodo Sign connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Businesses

Retrieves businesses from Xodo Sign.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xodoSign/latest/actions/list-businesses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xodoSign/latest/actions/list-businesses?${params}`, {
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
      "business_connection_id": "string",
      "business_id": 1,
      "business_identifier": "string",
      "business_name": "Ava Chen",
      "business_status": 1,
      "creation_time_stamp": 1,
      "is_primary": 1
    }
  ],
  "meta": {}
}
```

See the full [List Businesses action reference](actions/list-businesses.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/xodoSign/latest/actions/list-businesses).

## Create Bulk Job

Creates a new bulk job in Xodo Sign.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/xodoSign/latest/actions/create-bulk-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "business_id": "string",
  "templateHash": "string",
  "rows[]": [
    [
      "string"
    ]
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/xodoSign/latest/actions/create-bulk-job', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "business_id": "string",
    "templateHash": "string",
    "rows[]": [["string"]]
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
      "business_id": 1,
      "created_at": "2026-05-07T12:00:00.000Z",
      "document_count": 1,
      "entry_id": 1,
      "status": "string",
      "template_hash": "string",
      "user_id": 1
    }
  ],
  "meta": {}
}
```

See the full [Create Bulk Job action reference](actions/create-bulk-job.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/xodoSign/latest/actions/create-bulk-job).
