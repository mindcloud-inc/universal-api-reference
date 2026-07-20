# Company URL Finder Universal API Examples

These examples use the MindCloud API key and Company URL Finder connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Company Query to LinkedIn URL

Finds a company's LinkedIn URL in Company URL Finder.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/companyURLFinder/latest/actions/company-query-to-linkedin-url?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/companyURLFinder/latest/actions/company-query-to-linkedin-url?${params}`, {
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
      "exists": true,
      "linkedinUrl": "https://example.com",
      "remainingCredits": 1
    }
  ],
  "meta": {}
}
```

See the full [Company Query to LinkedIn URL action reference](actions/company-query-to-linkedin-url.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/companyURLFinder/latest/actions/company-query-to-linkedin-url).
