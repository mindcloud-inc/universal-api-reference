# Mailrelay Universal API Examples

These examples use the MindCloud API key and Mailrelay connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Ping

Retrieves API connectivity status from Mailrelay.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailrelay/latest/actions/ping?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailrelay/latest/actions/ping?${params}`, {
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
  "data": [],
  "meta": {}
}
```

See the full [Ping action reference](actions/ping.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mailrelay/latest/actions/ping).

## Bulk Update Subscribers

Updates multiple subscriber records in Mailrelay.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mailrelay/latest/actions/bulk-update-subscribers" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "bulkAction": "remove_from_group"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailrelay/latest/actions/bulk-update-subscribers', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "bulkAction": "remove_from_group"
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
      "id": 1
    }
  ],
  "meta": {}
}
```

See the full [Bulk Update Subscribers action reference](actions/bulk-update-subscribers.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mailrelay/latest/actions/bulk-update-subscribers).
