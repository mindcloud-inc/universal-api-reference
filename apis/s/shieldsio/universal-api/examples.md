# Shields.io Universal API Examples

These examples use the MindCloud API key and Shields.io connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Generate Static Badge

Retrieves a custom static badge image from Shields.io.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shieldsio/latest/actions/generate-static-badge?connectionId=$CONNECTION_ID&badgeContent=build-passing-brightgreen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "badgeContent": "build-passing-brightgreen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shieldsio/latest/actions/generate-static-badge?${params}`, {
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
        1
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Generate Static Badge action reference](actions/generate-static-badge.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/shieldsio/latest/actions/generate-static-badge).
