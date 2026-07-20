# KickFire Universal API Examples

These examples use the MindCloud API key and KickFire connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Company by Website

Retrieves company firmographic data from KickFire by website.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kickFire/latest/actions/get-company-by-website?connectionId=$CONNECTION_ID&website=example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "website": "example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kickFire/latest/actions/get-company-by-website?${params}`, {
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
      "data": [
        [
          {}
        ]
      ],
      "results": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Company by Website action reference](actions/get-company-by-website.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/kickFire/latest/actions/get-company-by-website).
