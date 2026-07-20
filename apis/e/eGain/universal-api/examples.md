# eGain Universal API Examples

These examples use the MindCloud API key and eGain connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Authentications

Retrieves a list of authentications from eGain.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eGain/latest/actions/list-authentications?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eGain/latest/actions/list-authentications?${params}`, {
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

See the full [List Authentications action reference](actions/list-authentications.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/eGain/latest/actions/list-authentications).

## Create Account

Creates a new account in eGain.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eGain/latest/actions/create-account" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "active": true,
  "address": "string",
  "channel.id": "string",
  "chatConfigurations.entryPoint.id": "string",
  "chatConfigurations.orchestration.id": "string",
  "chatConfigurations.timeout": 1,
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eGain/latest/actions/create-account', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "active": true,
    "address": "string",
    "channel.id": "string",
    "chatConfigurations.entryPoint.id": "string",
    "chatConfigurations.orchestration.id": "string",
    "chatConfigurations.timeout": 1,
    "name": "Ava Chen"
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

See the full [Create Account action reference](actions/create-account.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/eGain/latest/actions/create-account).
