# Socket Universal API Examples

These examples use the MindCloud API key and Socket connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Quota

Retrieves current API quota details from Socket.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/socket/latest/actions/get-quota?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/socket/latest/actions/get-quota?${params}`, {
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
      "maxQuota": 1,
      "nextWindowRefresh": "string",
      "quota": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Quota action reference](actions/get-quota.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/socket/latest/actions/get-quota).

## Associate Repository Label

Associates a repository label with a Socket repository.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/socket/latest/actions/associate-repository-label" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "labelId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/socket/latest/actions/associate-repository-label', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "labelId": "string"
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
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Associate Repository Label action reference](actions/associate-repository-label.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/socket/latest/actions/associate-repository-label).
