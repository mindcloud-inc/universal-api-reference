# Dungeon Fighter Online Universal API Examples

These examples use the MindCloud API key and Dungeon Fighter Online connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Servers

Retrieves server information from Dungeon Fighter Online.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dungeonFighterOnline/latest/actions/list-servers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dungeonFighterOnline/latest/actions/list-servers?${params}`, {
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
      "serverId": "string",
      "serverName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [List Servers action reference](actions/list-servers.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dungeonFighterOnline/latest/actions/list-servers).
