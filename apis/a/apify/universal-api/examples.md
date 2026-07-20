# Apify Universal API Examples

These examples use the MindCloud API key and Apify connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Private User Data

Retrieves private user data from Apify.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/apify/latest/actions/get-private-user-data?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/apify/latest/actions/get-private-user-data?${params}`, {
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

See the full [Get Private User Data action reference](actions/get-private-user-data.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/apify/latest/actions/get-private-user-data).
