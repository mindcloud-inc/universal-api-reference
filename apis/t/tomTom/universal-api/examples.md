# TomTom Universal API Examples

These examples use the MindCloud API key and TomTom connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List POI Categories

Retrieves available POI categories from TomTom.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tomTom/latest/actions/list-poi-categories?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tomTom/latest/actions/list-poi-categories?${params}`, {
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
      "childCategoryIds": [
        1
      ],
      "id": 1,
      "name": "Ava Chen",
      "synonyms": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

See the full [List POI Categories action reference](actions/list-poi-categories.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/tomTom/latest/actions/list-poi-categories).
