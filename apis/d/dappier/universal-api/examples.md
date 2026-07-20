# Dappier Universal API Examples

These examples use the MindCloud API key and Dappier connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Search Real Time Data

Retrieves a real-time AI search response from Dappier.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dappier/latest/actions/search-real-time-data?connectionId=$CONNECTION_ID&aiModelId=am_01j06ytn18ejftedz6dyhz2b15&query=What%20is%20the%20weather%20in%20Austin%20today%3F" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "aiModelId": "am_01j06ytn18ejftedz6dyhz2b15",
  "query": "What is the weather in Austin today?"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dappier/latest/actions/search-real-time-data?${params}`, {
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

See the full [Search Real Time Data action reference](actions/search-real-time-data.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dappier/latest/actions/search-real-time-data).
