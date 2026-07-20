# Scryfall Universal API Examples

These examples use the MindCloud API key and Scryfall connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Sets

Retrieves all card sets from Scryfall.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scryfall/latest/actions/list-sets?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scryfall/latest/actions/list-sets?${params}`, {
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
      "card_count": 1,
      "code": "string",
      "digital": true,
      "foil_only": true,
      "id": "string",
      "name": "Ava Chen",
      "nonfoil_only": true,
      "released_at": "2026-05-07T12:00:00.000Z",
      "scryfall_uri": "string",
      "set_type": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Sets action reference](actions/list-sets.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/scryfall/latest/actions/list-sets).
