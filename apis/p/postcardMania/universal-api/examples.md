# PostcardMania Universal API Examples

These examples use the MindCloud API key and PostcardMania connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Edit Designer Design

Retrieves an edit session for a PostcardMania design.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/postcardMania/latest/actions/edit-designer-design?connectionId=$CONNECTION_ID&designID=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "designID": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/postcardMania/latest/actions/edit-designer-design?${params}`, {
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
      "designID": 1,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Edit Designer Design action reference](actions/edit-designer-design.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/postcardMania/latest/actions/edit-designer-design).

## Add Favorite

Creates a new favorite design in PostcardMania.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/postcardMania/latest/actions/add-favorite" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "designID": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/postcardMania/latest/actions/add-favorite', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "designID": 1
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "createdDateTime": "2026-05-07T12:00:00.000Z",
      "designID": 1
    }
  ],
  "meta": {}
}
```

See the full [Add Favorite action reference](actions/add-favorite.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/postcardMania/latest/actions/add-favorite).
