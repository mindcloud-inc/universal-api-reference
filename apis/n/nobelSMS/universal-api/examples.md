# NobelSMS Universal API Examples

These examples use the MindCloud API key and NobelSMS connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Balances

Retrieves balances from NobelSMS.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nobelSMS/latest/actions/list-balances?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nobelSMS/latest/actions/list-balances?${params}`, {
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
      "balance": 1,
      "balance_updated": "string",
      "car_id": 1,
      "currency_code": "string",
      "descr": "string",
      "id": 1
    }
  ],
  "meta": {}
}
```

See the full [List Balances action reference](actions/list-balances.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/nobelSMS/latest/actions/list-balances).

## Create Blacklist Entry

Creates a new blacklist entry in NobelSMS.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/nobelSMS/latest/actions/create-blacklist-entry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "bnumber": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nobelSMS/latest/actions/create-blacklist-entry', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "bnumber": 1
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
      "id": 1
    }
  ],
  "meta": {}
}
```

See the full [Create Blacklist Entry action reference](actions/create-blacklist-entry.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/nobelSMS/latest/actions/create-blacklist-entry).
