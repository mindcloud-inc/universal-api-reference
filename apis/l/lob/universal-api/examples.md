# Lob Universal API Examples

These examples use the MindCloud API key and Lob connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Addresses



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lob/latest/actions/list-addresses?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lob/latest/actions/list-addresses?${params}`, {
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
      "count": 1,
      "data": [
        {}
      ],
      "next_url": "https://example.com",
      "object": "string",
      "previous_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [List Addresses action reference](actions/list-addresses.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/lob/latest/actions/list-addresses).

## Bulk Verify International Addresses



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/lob/latest/actions/bulk-verify-international-addresses" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "addresses[]": [
    {}
  ],
  "addresses[].primaryLine": "string",
  "addresses[].country": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lob/latest/actions/bulk-verify-international-addresses', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "addresses[]": [{}],
    "addresses[].primaryLine": "string",
    "addresses[].country": "string"
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
      "addresses": [
        {}
      ],
      "errors": true
    }
  ],
  "meta": {}
}
```

See the full [Bulk Verify International Addresses action reference](actions/bulk-verify-international-addresses.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/lob/latest/actions/bulk-verify-international-addresses).
