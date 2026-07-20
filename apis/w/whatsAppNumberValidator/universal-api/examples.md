# WhatsApp Number Validator Universal API Examples

These examples use the MindCloud API key and WhatsApp Number Validator connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Validate WhatsApp Number

Retrieves WhatsApp number validation details from WhatsApp Number Validator.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whatsAppNumberValidator/latest/actions/validate-whats-app-number?connectionId=$CONNECTION_ID&number=14083742784" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "number": "14083742784"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/whatsAppNumberValidator/latest/actions/validate-whats-app-number?${params}`, {
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

See the full [Validate WhatsApp Number action reference](actions/validate-whats-app-number.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/whatsAppNumberValidator/latest/actions/validate-whats-app-number).
