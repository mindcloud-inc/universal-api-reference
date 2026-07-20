# AeroLeads Universal API Examples

These examples use the MindCloud API key and AeroLeads connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Company Email



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aeroLeads/latest/actions/get-company-email?connectionId=$CONNECTION_ID&firstName=John&lastName=Doe&company=Acme%20Inc" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "firstName": "John",
  "lastName": "Doe",
  "company": "Acme Inc"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aeroLeads/latest/actions/get-company-email?${params}`, {
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

See the full [Get Company Email action reference](actions/get-company-email.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/aeroLeads/latest/actions/get-company-email).
