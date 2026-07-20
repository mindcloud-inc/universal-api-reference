# Abstract IP Intelligence Universal API Examples

These examples use the MindCloud API key and Abstract IP Intelligence connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get IP Intelligence

Retrieves IP intelligence from Abstract IP Intelligence.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/abstractIPIntelligence/latest/actions/get-ip-intelligence?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/abstractIPIntelligence/latest/actions/get-ip-intelligence?${params}`, {
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
      "asn": {},
      "company": {},
      "currency": {},
      "domains": {},
      "flag": {},
      "ip_address": "string",
      "location": {},
      "security": {},
      "timezone": {}
    }
  ],
  "meta": {}
}
```

See the full [Get IP Intelligence action reference](actions/get-ip-intelligence.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/abstractIPIntelligence/latest/actions/get-ip-intelligence).
