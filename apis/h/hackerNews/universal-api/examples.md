# Hacker News Universal API Examples

These examples use the MindCloud API key and Hacker News connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Max Item ID

Retrieves the maximum item ID from Hacker News.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hackerNews/latest/actions/get-max-item-id?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hackerNews/latest/actions/get-max-item-id?${params}`, {
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
      "value": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Max Item ID action reference](actions/get-max-item-id.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/hackerNews/latest/actions/get-max-item-id).
