# Dremio Universal API Examples

These examples use the MindCloud API key and Dremio connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Catalog

Retrieves catalog entries from a Dremio project.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dremio/latest/actions/list-catalog?connectionId=$CONNECTION_ID&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dremio/latest/actions/list-catalog?${params}`, {
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
      "data": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Catalog action reference](actions/list-catalog.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dremio/latest/actions/list-catalog).

## Cancel Job

Cancels a job in a Dremio project.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/dremio/latest/actions/cancel-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "projectId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dremio/latest/actions/cancel-job', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "projectId": "string"
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

See the full [Cancel Job action reference](actions/cancel-job.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dremio/latest/actions/cancel-job).
