# AvoSMS Universal API Examples

These examples use the MindCloud API key and AvoSMS connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account Balance

Retrieves your account balance from AvoSMS.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/avoSMS/latest/actions/get-account-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/avoSMS/latest/actions/get-account-balance?${params}`, {
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

See the full [Get Account Balance action reference](actions/get-account-balance.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/avoSMS/latest/actions/get-account-balance).

## Add Contact

Creates a new contact in AvoSMS.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/avoSMS/latest/actions/add-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "listContactId": "12345",
  "contactTelephoneNumber": "33612345678"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/avoSMS/latest/actions/add-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "listContactId": "12345",
    "contactTelephoneNumber": "33612345678"
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

See the full [Add Contact action reference](actions/add-contact.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/avoSMS/latest/actions/add-contact).
