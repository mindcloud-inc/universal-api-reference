# Upstash Redis Universal API Examples

These examples use the MindCloud API key and Upstash Redis connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Ping

Retrieves a ping response from Upstash Redis.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/upstashRedis/latest/actions/ping?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/upstashRedis/latest/actions/ping?${params}`, {
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
      "result": "string"
    }
  ],
  "meta": {}
}
```

See the full [Ping action reference](actions/ping.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/upstashRedis/latest/actions/ping).

## ACL

Executes the ACL command in Upstash Redis to manage access control list.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/upstashRedis/latest/actions/acl" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/upstashRedis/latest/actions/acl', {
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

See the full [ACL action reference](actions/acl.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/upstashRedis/latest/actions/acl).
