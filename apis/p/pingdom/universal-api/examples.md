# Pingdom Universal API Examples

These examples use the MindCloud API key and Pingdom connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Credits



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pingdom/latest/actions/get-credits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pingdom/latest/actions/get-credits?${params}`, {
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
      "autofillsms": true,
      "autofillsmsAmount": 1,
      "autofillsmsWhenLeft": 1,
      "availablealertingfullusers": 1,
      "availablechecks": 1,
      "availabledefaultchecks": 1,
      "availablerumsites": 1,
      "availablesms": 1,
      "availablesmstests": 1,
      "availabletransactionchecks": 1,
      "checklimit": 1,
      "defaultchecklimit": 1,
      "maxalertingfullusers": 1,
      "maxrumfilters": 1,
      "maxrumpageviews": 1,
      "maxSmsOverage": 1,
      "transactionchecklimit": 1,
      "useddefault": 1,
      "usedrumsites": 1,
      "usedtransaction": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Credits action reference](actions/get-credits.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pingdom/latest/actions/get-credits).

## Create Check



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pingdom/latest/actions/create-check" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "host": "string",
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pingdom/latest/actions/create-check', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "host": "string",
    "type": "string"
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
      "id": 1,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Create Check action reference](actions/create-check.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pingdom/latest/actions/create-check).
