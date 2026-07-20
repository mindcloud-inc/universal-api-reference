# Returnless Universal API Examples

These examples use the MindCloud API key and Returnless connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current Account

Retrieves the current account from Returnless.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/returnless/latest/actions/get-current-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/returnless/latest/actions/get-current-account?${params}`, {
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
      "data": {},
      "meta": {}
    }
  ],
  "meta": {}
}
```

See the full [Get Current Account action reference](actions/get-current-account.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/returnless/latest/actions/get-current-account).

## Add Return Order Item

Adds an item to a return order in Returnless.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/returnless/latest/actions/add-return-order-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "returnOrder": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/returnless/latest/actions/add-return-order-item', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "returnOrder": "string"
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
      "data": {},
      "meta": {}
    }
  ],
  "meta": {}
}
```

See the full [Add Return Order Item action reference](actions/add-return-order-item.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/returnless/latest/actions/add-return-order-item).
