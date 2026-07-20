# SMSGlobal Universal API Examples

These examples use the MindCloud API key and SMSGlobal connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get User Contact Details

Retrieves contact details for the authenticated SMSGlobal account.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sMSGlobal/latest/actions/get-user-contact-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sMSGlobal/latest/actions/get-user-contact-details?${params}`, {
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
      "address": "string",
      "city": "string",
      "country": "string",
      "email": "ava@example.com",
      "id": 1,
      "name": "Ava Chen",
      "phone": "string",
      "postcode": "string",
      "state": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get User Contact Details action reference](actions/get-user-contact-details.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sMSGlobal/latest/actions/get-user-contact-details).
