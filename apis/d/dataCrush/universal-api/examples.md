# DataCrush Universal API Examples

These examples use the MindCloud API key and DataCrush connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Search Contacts

Finds contacts in DataCrush by email address.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dataCrush/latest/actions/search-contacts?connectionId=$CONNECTION_ID&email=name%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "name@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dataCrush/latest/actions/search-contacts?${params}`, {
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
      "result": "string",
      "rows": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Search Contacts action reference](actions/search-contacts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dataCrush/latest/actions/search-contacts).

## Add Contact To Account

Adds a contact to an account in DataCrush.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/dataCrush/latest/actions/add-contact-to-account" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "account_key": "string",
  "contact_key": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dataCrush/latest/actions/add-contact-to-account', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "account_key": "string",
    "contact_key": "string"
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

See the full [Add Contact To Account action reference](actions/add-contact-to-account.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dataCrush/latest/actions/add-contact-to-account).
