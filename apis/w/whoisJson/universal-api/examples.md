# WhoisJson Universal API Examples

These examples use the MindCloud API key and WhoisJson connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Whois Data

Retrieves WHOIS data for a domain from WhoisJson.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whoisJson/latest/actions/get-whois-data?connectionId=$CONNECTION_ID&domain=example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domain": "example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/whoisJson/latest/actions/get-whois-data?${params}`, {
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
      "changed": "2026-05-07T12:00:00.000Z",
      "created": "2026-05-07T12:00:00.000Z",
      "expires": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "nameserver": [
        "Ava Chen"
      ],
      "registered": true,
      "registrar": {
        "name": "Ava Chen",
        "url": "https://example.com"
      },
      "status": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

See the full [Get Whois Data action reference](actions/get-whois-data.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/whoisJson/latest/actions/get-whois-data).
