# CallRail Universal API Examples

These examples use the MindCloud API key and CallRail connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Accounts

Retrieves accounts from CallRail.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/callRail/latest/actions/list-accounts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/callRail/latest/actions/list-accounts?${params}`, {
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
      "agencyInTrial": true,
      "brandStatus": "string",
      "createdAt": "string",
      "hasZuoraAccount": true,
      "hipaaAccount": true,
      "id": "string",
      "inboundRecordingEnabled": true,
      "name": "Ava Chen",
      "numericId": 1,
      "outboundRecordingEnabled": true
    }
  ],
  "meta": {}
}
```

See the full [List Accounts action reference](actions/list-accounts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/callRail/latest/actions/list-accounts).

## Create Company

Creates a company in CallRail.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/callRail/latest/actions/create-company" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "account_id": "string",
  "name": "Ava Chen",
  "time_zone": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/callRail/latest/actions/create-company', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "account_id": "string",
    "name": "Ava Chen",
    "time_zone": "string"
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
      "callscoreEnabled": true,
      "callscribeEnabled": true,
      "createdAt": "string",
      "disabledAt": "string",
      "dniActive": "string",
      "formCapture": true,
      "id": "string",
      "keywordSpottingEnabled": "string",
      "leadScoringEnabled": true,
      "name": "Ava Chen",
      "scriptUrl": "https://example.com",
      "status": "string",
      "swapCookieDuration": 1,
      "swapCookieDurationUnit": "string",
      "swapExcludeJquery": "string",
      "swapLandingOverride": "string",
      "swapPpcOverride": "string",
      "timeZone": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Company action reference](actions/create-company.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/callRail/latest/actions/create-company).
