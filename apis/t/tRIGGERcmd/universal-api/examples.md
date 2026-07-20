# TRIGGERcmd Universal API Examples

These examples use the MindCloud API key and TRIGGERcmd connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Commands

Retrieves a list of commands from TRIGGERcmd.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tRIGGERcmd/latest/actions/list-commands?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tRIGGERcmd/latest/actions/list-commands?${params}`, {
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
  "data": [],
  "meta": {}
}
```

See the full [List Commands action reference](actions/list-commands.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/tRIGGERcmd/latest/actions/list-commands).

## Trigger Command

Triggers a command on a computer in TRIGGERcmd.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tRIGGERcmd/latest/actions/trigger-command" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "computer": "string",
  "trigger": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tRIGGERcmd/latest/actions/trigger-command', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "computer": "string",
    "trigger": "string"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [],
  "meta": {}
}
```

See the full [Trigger Command action reference](actions/trigger-command.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/tRIGGERcmd/latest/actions/trigger-command).
