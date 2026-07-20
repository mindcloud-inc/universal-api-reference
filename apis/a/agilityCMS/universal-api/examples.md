# Agility CMS Universal API Examples

These examples use the MindCloud API key and Agility CMS connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Sitemap Flat (Preview)

Retrieves the preview sitemap as a flat list from Agility CMS.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/agilityCMS/latest/actions/get-sitemap-flat-preview?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/agilityCMS/latest/actions/get-sitemap-flat-preview?${params}`, {
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

See the full [Get Sitemap Flat (Preview) action reference](actions/get-sitemap-flat-preview.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/agilityCMS/latest/actions/get-sitemap-flat-preview).
