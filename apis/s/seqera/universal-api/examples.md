# Seqera Universal API Examples

These examples use the MindCloud API key and Seqera connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Credentials

Retrieves available credentials from Seqera.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seqera/latest/actions/list-credentials?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seqera/latest/actions/list-credentials?${params}`, {
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
      "credentials": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Credentials action reference](actions/list-credentials.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/seqera/latest/actions/list-credentials).

## Cancel Run

Cancels a workflow run in Seqera.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/seqera/latest/actions/cancel-run" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "run_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/seqera/latest/actions/cancel-run', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "run_id": "string"
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

See the full [Cancel Run action reference](actions/cancel-run.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/seqera/latest/actions/cancel-run).
