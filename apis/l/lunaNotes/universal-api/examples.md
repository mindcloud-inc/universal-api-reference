# LunaNotes Universal API Examples

These examples use the MindCloud API key and LunaNotes connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Notes

Retrieves notes from LunaNotes.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lunaNotes/latest/actions/list-notes?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lunaNotes/latest/actions/list-notes?${params}`, {
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
      "authorId": "string",
      "content": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "draft": true,
      "icon": "string",
      "iconColor": "string",
      "id": "string",
      "isPublic": true,
      "json": {},
      "published": true,
      "status": "string",
      "timeEnd": 1,
      "timeStart": 1,
      "title": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "v": "string",
      "videoId": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Notes action reference](actions/list-notes.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/lunaNotes/latest/actions/list-notes).
