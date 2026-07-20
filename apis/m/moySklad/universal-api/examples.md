# MoySklad Universal API Examples

These examples use the MindCloud API key and MoySklad connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List products

Retrieves products from MoySklad.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moySklad/latest/actions/list-products?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moySklad/latest/actions/list-products?${params}`, {
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
      "code": "string",
      "context": {},
      "externalCode": "string",
      "id": "string",
      "meta": {},
      "name": "Ava Chen",
      "rows": [
        {}
      ],
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [List products action reference](actions/list-products.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/moySklad/latest/actions/list-products).

## Create counterparty

Creates a counterparty in MoySklad.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/moySklad/latest/actions/create-counterparty" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moySklad/latest/actions/create-counterparty', {
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
      "id": "string",
      "meta": {},
      "name": "Ava Chen",
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Create counterparty action reference](actions/create-counterparty.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/moySklad/latest/actions/create-counterparty).
