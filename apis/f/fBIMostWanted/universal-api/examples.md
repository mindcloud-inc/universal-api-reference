# FBI Most Wanted Universal API Examples

These examples use the MindCloud API key and FBI Most Wanted connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Wanted Records

Retrieves wanted records from FBI Most Wanted.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fBIMostWanted/latest/actions/list-wanted-records?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fBIMostWanted/latest/actions/list-wanted-records?${params}`, {
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
      "caution": "string",
      "description": "string",
      "details": "string",
      "eyes": "string",
      "field_offices": [
        "string"
      ],
      "files": [
        {}
      ],
      "hair": "string",
      "height_max": 1,
      "height_min": 1,
      "images": [
        {}
      ],
      "modified": "2026-05-07T12:00:00.000Z",
      "path": "string",
      "pathId": "string",
      "poster_classification": "string",
      "publication": "2026-05-07T12:00:00.000Z",
      "race": "string",
      "remarks": "string",
      "reward_max": 1,
      "reward_min": 1,
      "reward_text": "string",
      "sex": "string",
      "status": "string",
      "subjects": [
        "string"
      ],
      "title": "string",
      "uid": "string",
      "url": "https://example.com",
      "warning_message": "string",
      "weight_max": 1,
      "weight_min": 1
    }
  ],
  "meta": {}
}
```

See the full [List Wanted Records action reference](actions/list-wanted-records.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/fBIMostWanted/latest/actions/list-wanted-records).
