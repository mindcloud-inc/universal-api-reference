# Fintoc Universal API Examples

These examples use the MindCloud API key and Fintoc connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Accounts

Retrieves accounts from Fintoc.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fintoc/latest/actions/list-accounts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fintoc/latest/actions/list-accounts?${params}`, {
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
      "available_balance": 1,
      "currency": "string",
      "description": "string",
      "entity": {},
      "id": "string",
      "is_root": true,
      "mode": "string",
      "object": "string",
      "root_account_number": "string",
      "root_account_number_id": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Accounts action reference](actions/list-accounts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/fintoc/latest/actions/list-accounts).

## Create Link Intent

Creates a link intent in Fintoc.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fintoc/latest/actions/create-link-intent" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "product": "movements",
  "holderType": "individual",
  "country": "cl"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fintoc/latest/actions/create-link-intent', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "product": "movements",
    "holderType": "individual",
    "country": "cl"
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
      "country": "string",
      "created_at": "string",
      "exchange_token": "string",
      "exchange_token_expires_at": "string",
      "holder_type": "string",
      "id": "string",
      "mode": "string",
      "object": "string",
      "product": "string",
      "status": "string",
      "widget_token": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Link Intent action reference](actions/create-link-intent.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/fintoc/latest/actions/create-link-intent).
