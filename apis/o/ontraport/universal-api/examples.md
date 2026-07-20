# Ontraport Universal API Examples

These examples use the MindCloud API key and Ontraport connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Retrieve Contact Object Meta

Retrieves metadata for contact objects in Ontraport.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ontraport/latest/actions/retrieve-contact-object-meta?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ontraport/latest/actions/retrieve-contact-object-meta?${params}`, {
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

See the full [Retrieve Contact Object Meta action reference](actions/retrieve-contact-object-meta.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/ontraport/latest/actions/retrieve-contact-object-meta).
