# Apideck Universal API Examples

These examples use the MindCloud API key and Apideck connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get all consumers

Retrieves all consumers from Apideck Vault.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/apideck/latest/actions/consumersall?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/apideck/latest/actions/consumersall?${params}`, {
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
      "aggregated_request_count": 1,
      "application_id": "string",
      "consumer_id": "string",
      "created": "string",
      "metadata": {},
      "modified": "string",
      "request_count_updated": "string",
      "request_counts": {},
      "services": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

See the full [Get all consumers action reference](actions/consumersall.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/apideck/latest/actions/consumersall).

## Update consent state

Updates a connection consent state in Apideck Vault.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/apideck/latest/actions/connectionconsentupdate" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "service_id": "string",
  "unified_api": "string",
  "resources": {},
  "granted": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/apideck/latest/actions/connectionconsentupdate', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "service_id": "string",
    "unified_api": "string",
    "resources": {},
    "granted": true
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
      "created_at": "string",
      "granted": true,
      "id": "string",
      "resources": {}
    }
  ],
  "meta": {}
}
```

See the full [Update consent state action reference](actions/connectionconsentupdate.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/apideck/latest/actions/connectionconsentupdate).
