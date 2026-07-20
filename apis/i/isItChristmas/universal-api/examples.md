# Is It Christmas? Universal API Examples

These examples use the MindCloud API key and Is It Christmas? connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Christmases



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/isItChristmas/latest/actions/list-christmases?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/isItChristmas/latest/actions/list-christmases?${params}`, {
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
      "answer": "string",
      "christmas": true,
      "christmas_day": "2026-05-07T12:00:00.000Z",
      "christmas_time": 1,
      "country": "string",
      "country_names": [
        "Ava Chen"
      ],
      "id": "string",
      "timezone": "string",
      "year": 1
    }
  ],
  "meta": {}
}
```

See the full [List Christmases action reference](actions/list-christmases.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/isItChristmas/latest/actions/list-christmases).
