# Logo.dev Universal API Examples

These examples use the MindCloud API key and Logo.dev connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Search Company Domains

Finds company domains in Logo.dev.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/logodev/latest/actions/search-company-domains?connectionId=$CONNECTION_ID&q=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "q": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/logodev/latest/actions/search-company-domains?${params}`, {
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
      "domain": "string",
      "logo_url": "https://example.com",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Search Company Domains action reference](actions/search-company-domains.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/logodev/latest/actions/search-company-domains).
