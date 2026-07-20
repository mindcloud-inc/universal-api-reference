# BoxHero Universal API Examples

These examples use the MindCloud API key and BoxHero connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Linked Team

Retrieves the linked team from BoxHero.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/boxHero/latest/actions/get-linked-team?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/boxHero/latest/actions/get-linked-team?${params}`, {
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
      "currency_symbol": "string",
      "id": 1,
      "memo": "string",
      "mode": 1,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Get Linked Team action reference](actions/get-linked-team.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/boxHero/latest/actions/get-linked-team).

## Create Item

Creates a new item in BoxHero.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/boxHero/latest/actions/create-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/boxHero/latest/actions/create-item', {
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
      "id": 1
    }
  ],
  "meta": {}
}
```

See the full [Create Item action reference](actions/create-item.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/boxHero/latest/actions/create-item).
