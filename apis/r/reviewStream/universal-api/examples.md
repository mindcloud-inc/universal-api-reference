# ReviewStream Universal API Examples

These examples use the MindCloud API key and ReviewStream connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Reviews

Retrieves reviews from ReviewStream.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reviewStream/latest/actions/list-reviews?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reviewStream/latest/actions/list-reviews?${params}`, {
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

See the full [List Reviews action reference](actions/list-reviews.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/reviewStream/latest/actions/list-reviews).
