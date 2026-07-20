# Magileads Universal API Examples

These examples use the MindCloud API key and Magileads connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List PRM Statuses

Retrieves your PRM statuses from Magileads.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/magileads/latest/actions/list-prm-statuses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/magileads/latest/actions/list-prm-statuses?${params}`, {
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
      "state": true,
      "status": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [List PRM Statuses action reference](actions/list-prm-statuses.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/magileads/latest/actions/list-prm-statuses).

## Create Blacklist

Creates a new blacklist in Magileads.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/magileads/latest/actions/create-blacklist" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/magileads/latest/actions/create-blacklist', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
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
      "blacklist_id": 1,
      "state": true
    }
  ],
  "meta": {}
}
```

See the full [Create Blacklist action reference](actions/create-blacklist.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/magileads/latest/actions/create-blacklist).
