# SEO GPT Universal API Examples

These examples use the MindCloud API key and SEO GPT connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Generate SEO Title



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sEOGPT/latest/actions/generate-seo-title?connectionId=$CONNECTION_ID&kw=best%20running%20shoes" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "kw": "best running shoes"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sEOGPT/latest/actions/generate-seo-title?${params}`, {
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
      "response": "string"
    }
  ],
  "meta": {}
}
```

See the full [Generate SEO Title action reference](actions/generate-seo-title.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sEOGPT/latest/actions/generate-seo-title).
