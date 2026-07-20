# Agiliron Universal API Examples

These examples use the MindCloud API key and Agiliron connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Read Contact

Retrieves contact records from Agiliron.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/agiliron/latest/actions/read-contact?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/agiliron/latest/actions/read-contact?${params}`, {
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
  "data": [],
  "meta": {}
}
```

See the full [Read Contact action reference](actions/read-contact.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/agiliron/latest/actions/read-contact).

## Add Account

Creates a new account in Agiliron.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/agiliron/latest/actions/add-account" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/agiliron/latest/actions/add-account', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [],
  "meta": {}
}
```

See the full [Add Account action reference](actions/add-account.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/agiliron/latest/actions/add-account).
