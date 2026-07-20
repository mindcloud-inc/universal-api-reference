# Modern Treasury Universal API Examples

These examples use the MindCloud API key and Modern Treasury connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Internal Accounts

Retrieves internal accounts from Modern Treasury.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/modernTreasury/latest/actions/list-internal-accounts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/modernTreasury/latest/actions/list-internal-accounts?${params}`, {
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
      "accountCapabilities": {},
      "accountDetails": [
        {}
      ],
      "accountType": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "liveMode": true,
      "name": "Ava Chen",
      "object": "string",
      "partyAddress": {},
      "partyName": "Ava Chen",
      "partyType": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [List Internal Accounts action reference](actions/list-internal-accounts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/modernTreasury/latest/actions/list-internal-accounts).
