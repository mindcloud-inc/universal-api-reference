# Pinecone Universal API Examples

These examples use the MindCloud API key and Pinecone connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Describe Backup

Retrieves details for a backup from Pinecone.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pinecone/latest/actions/describe-backup?connectionId=$CONNECTION_ID&backupId=bbe4c309-c63e-4770-8550-b18ee77b87bd" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "backupId": "bbe4c309-c63e-4770-8550-b18ee77b87bd"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pinecone/latest/actions/describe-backup?${params}`, {
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
      "backup_id": "string",
      "cloud": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "dimension": 1,
      "name": "Ava Chen",
      "namespace_count": 1,
      "record_count": 1,
      "region": "string",
      "size_bytes": 1,
      "source_index_id": "string",
      "source_index_name": "Ava Chen",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Describe Backup action reference](actions/describe-backup.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pinecone/latest/actions/describe-backup).

## Configure Index

Updates an existing index in Pinecone.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pinecone/latest/actions/configure-index" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "indexName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pinecone/latest/actions/configure-index', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "indexName": "Ava Chen"
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
      "deletion_protection": "string",
      "dimension": 1,
      "host": "string",
      "metric": "string",
      "name": "Ava Chen",
      "spec": {
        "serverless": {
          "cloud": "string",
          "read_capacity": {
            "mode": "string",
            "status": {
              "state": "string"
            }
          },
          "region": "string"
        }
      },
      "status": {
        "ready": true,
        "state": "string"
      },
      "tags": {
        "kind": "string",
        "stage": "string"
      },
      "vector_type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Configure Index action reference](actions/configure-index.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pinecone/latest/actions/configure-index).
