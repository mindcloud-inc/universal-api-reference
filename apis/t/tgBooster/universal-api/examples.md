# TgBooster Universal API Examples

These examples use the MindCloud API key and TgBooster connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Cabinets

Retrieves Telegram Ads cabinets from TgBooster.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tgBooster/latest/actions/list-cabinets?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tgBooster/latest/actions/list-cabinets?${params}`, {
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
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "name": "Ava Chen",
      "photo": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [List Cabinets action reference](actions/list-cabinets.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/tgBooster/latest/actions/list-cabinets).
