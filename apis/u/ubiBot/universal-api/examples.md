# UbiBot Universal API Examples

These examples use the MindCloud API key and UbiBot connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Supported Timezones

Retrieves supported platform timezones from UbiBot.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ubiBot/latest/actions/list-supported-timezones?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ubiBot/latest/actions/list-supported-timezones?${params}`, {
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
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [List Supported Timezones action reference](actions/list-supported-timezones.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/ubiBot/latest/actions/list-supported-timezones).

## Add Command

Creates a device command in UbiBot.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ubiBot/latest/actions/add-command" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ubiBot/latest/actions/add-command', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
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
      "desp": "string",
      "errorCode": "string",
      "result": "string",
      "server_time": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Add Command action reference](actions/add-command.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/ubiBot/latest/actions/add-command).
