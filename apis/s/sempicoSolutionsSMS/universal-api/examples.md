# Sempico Solutions SMS Universal API Examples

These examples use the MindCloud API key and Sempico Solutions SMS connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account Information



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sempicoSolutionsSMS/latest/actions/get-account-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sempicoSolutionsSMS/latest/actions/get-account-information?${params}`, {
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
      "balance_daily_block": true,
      "balance_limit": 1,
      "balance_units": 1,
      "block": true,
      "can_send_bulk": true,
      "can_send_restapi": true,
      "company_name": "Ava Chen",
      "confirmed": 1,
      "currency": "string",
      "e_mail": "string",
      "finance": {},
      "id_subparent": 1,
      "login": "string",
      "name": "Ava Chen",
      "phone": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Account Information action reference](actions/get-account-information.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sempicoSolutionsSMS/latest/actions/get-account-information).

## Add Numbers to Blacklist



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sempicoSolutionsSMS/latest/actions/add-numbers-to-blacklist" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "numbers[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sempicoSolutionsSMS/latest/actions/add-numbers-to-blacklist', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "numbers[]": ["string"]
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
      "blacklistDetails": {
        "countAfter": 1,
        "countBefore": 1
      }
    }
  ],
  "meta": {}
}
```

See the full [Add Numbers to Blacklist action reference](actions/add-numbers-to-blacklist.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sempicoSolutionsSMS/latest/actions/add-numbers-to-blacklist).
