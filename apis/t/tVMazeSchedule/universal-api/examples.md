# TVMaze Schedule Universal API Examples

These examples use the MindCloud API key and TVMaze Schedule connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Alternate List

Retrieves an alternate list from TVMaze.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tVMazeSchedule/latest/actions/get-alternate-list?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tVMazeSchedule/latest/actions/get-alternate-list?${params}`, {
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
      "_links": {},
      "broadcast_premiere": true,
      "country_premiere": true,
      "dvd_release": true,
      "id": 1,
      "language": {},
      "language_premiere": true,
      "network": {},
      "streaming_premiere": true,
      "url": "https://example.com",
      "verbatim_order": true,
      "webChannel": {}
    }
  ],
  "meta": {}
}
```

See the full [Get Alternate List action reference](actions/get-alternate-list.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/tVMazeSchedule/latest/actions/get-alternate-list).
