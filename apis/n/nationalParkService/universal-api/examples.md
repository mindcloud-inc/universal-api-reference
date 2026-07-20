# National Park Service Universal API Examples

These examples use the MindCloud API key and National Park Service connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Parks

Retrieves parks from National Park Service.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nationalParkService/latest/actions/list-parks?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nationalParkService/latest/actions/list-parks?${params}`, {
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
      "data": [
        {}
      ],
      "limit": "string",
      "start": "string",
      "total": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Parks action reference](actions/list-parks.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/nationalParkService/latest/actions/list-parks).
