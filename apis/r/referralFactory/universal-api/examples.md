# Referral Factory Universal API Examples

These examples use the MindCloud API key and Referral Factory connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Campaigns

Retrieves campaigns from Referral Factory.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/referralFactory/latest/actions/list-campaigns?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/referralFactory/latest/actions/list-campaigns?${params}`, {
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
      "assets": {},
      "code": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "ends_at": "2026-05-07T12:00:00.000Z",
      "fields": {},
      "id": 1,
      "lang": "string",
      "name": "Ava Chen",
      "starts_at": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [List Campaigns action reference](actions/list-campaigns.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/referralFactory/latest/actions/list-campaigns).
