# Ambee Universal API Examples

These examples use the MindCloud API key and Ambee connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Geocode By Place

Retrieves location coordinates in Ambee by place name.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ambee/latest/actions/geocode-by-place?connectionId=$CONNECTION_ID&place=new%20york" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "place": "new york"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ambee/latest/actions/geocode-by-place?${params}`, {
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

See the full [Geocode By Place action reference](actions/geocode-by-place.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/ambee/latest/actions/geocode-by-place).
