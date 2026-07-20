# Fivetran Universal API Examples

These examples use the MindCloud API key and Fivetran connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account Info

Retrieves account details for your Fivetran account.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fivetran/latest/actions/get-account-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fivetran/latest/actions/get-account-info?${params}`, {
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
      "accountId": "string",
      "accountName": "Ava Chen",
      "systemKeyId": "string",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Account Info action reference](actions/get-account-info.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/fivetran/latest/actions/get-account-info).

## Create Connect Card

Creates a Connect Card for a connection in Fivetran.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fivetran/latest/actions/create-connect-card" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fivetran/latest/actions/create-connect-card', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "connectionId": "string"
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
      "connectCardToken": "string",
      "connectCardUri": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Connect Card action reference](actions/create-connect-card.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/fivetran/latest/actions/create-connect-card).
