# Refuge Restrooms Universal API Examples

These examples use the MindCloud API key and Refuge Restrooms connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Restrooms



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/refugeRestrooms/latest/actions/list-restrooms?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/refugeRestrooms/latest/actions/list-restrooms?${params}`, {
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
      "accessible": true,
      "approved": true,
      "changing_table": true,
      "city": "string",
      "comment": "string",
      "country": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "directions": "string",
      "downvote": 1,
      "edit_id": 1,
      "id": 1,
      "latitude": 1,
      "longitude": 1,
      "name": "Ava Chen",
      "state": "string",
      "street": "string",
      "unisex": true,
      "updated_at": "2026-05-07T12:00:00.000Z",
      "upvote": 1
    }
  ],
  "meta": {}
}
```

See the full [List Restrooms action reference](actions/list-restrooms.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/refugeRestrooms/latest/actions/list-restrooms).
