# ESRI Universal API Examples

These examples use the MindCloud API key and ESRI connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Portal Self

Retrieves the current ArcGIS portal view.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eSRI/latest/actions/portal-self?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eSRI/latest/actions/portal-self?${params}`, {
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
      "access": "string",
      "allSSL": true,
      "id": "string",
      "isPortal": true,
      "name": "Ava Chen",
      "urlKey": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Portal Self action reference](actions/portal-self.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/eSRI/latest/actions/portal-self).
