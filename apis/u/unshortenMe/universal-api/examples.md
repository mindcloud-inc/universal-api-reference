# Unshorten.Me Universal API Examples

These examples use the MindCloud API key and Unshorten.Me connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Unshorten URL

Retrieves an unshortened destination URL from Unshorten.Me.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/unshortenMe/latest/actions/unshorten-url?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fbit.ly%2F3DKWm5t" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://bit.ly/3DKWm5t"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/unshortenMe/latest/actions/unshorten-url?${params}`, {
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
      "shortened_url": "https://example.com",
      "success": true,
      "unshortened_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Unshorten URL action reference](actions/unshorten-url.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/unshortenMe/latest/actions/unshorten-url).
