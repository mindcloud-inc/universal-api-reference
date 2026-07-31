# Cataas Universal API Examples

These examples use the MindCloud API key and Cataas connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Count Cats



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cataas/latest/actions/count-cats?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cataas/latest/actions/count-cats?${params}`, {
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
      "count": 1
    }
  ],
  "meta": {}
}
```

See the full [Count Cats action reference](actions/count-cats.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cataas/latest/actions/count-cats).
