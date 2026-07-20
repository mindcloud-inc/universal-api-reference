# Formilla Universal API Examples

These examples use the MindCloud API key and Formilla connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Create or Update Contact (Email Required)

Creates or updates a contact in Formilla by email address.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/formilla/latest/actions/upsert-contact-by-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "customer@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/formilla/latest/actions/upsert-contact-by-email', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "customer@example.com"
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

See the full [Create or Update Contact (Email Required) action reference](actions/upsert-contact-by-email.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/formilla/latest/actions/upsert-contact-by-email).
