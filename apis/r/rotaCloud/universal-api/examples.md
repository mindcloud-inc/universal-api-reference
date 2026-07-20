# RotaCloud Universal API Examples

These examples use the MindCloud API key and RotaCloud connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Accounts

Lists accounts in RotaCloud.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/list-accounts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/list-accounts?${params}`, {
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
      "billing_term": "string",
      "billing_type": "string",
      "created": "string",
      "expired": true,
      "features_disabled": [
        "string"
      ],
      "id": 1,
      "industry": 1,
      "level": "string",
      "name": "Ava Chen",
      "owner": 1,
      "permissions": [
        "string"
      ],
      "services": [
        {}
      ],
      "setup_steps": [
        {}
      ],
      "suspended": true,
      "timezone": 1,
      "total_employees": 1
    }
  ],
  "meta": {}
}
```

See the full [List Accounts action reference](actions/list-accounts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/rotaCloud/latest/actions/list-accounts).

## Acknowledge Shifts

Acknowledges shifts in RotaCloud.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/acknowledge-shifts" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "shifts[]": [
    1
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/acknowledge-shifts', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "shifts[]": [1]
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
      "result": "string"
    }
  ],
  "meta": {}
}
```

See the full [Acknowledge Shifts action reference](actions/acknowledge-shifts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/rotaCloud/latest/actions/acknowledge-shifts).
