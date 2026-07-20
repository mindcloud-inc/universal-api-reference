# Email List Validation Universal API Examples

These examples use the MindCloud API key and Email List Validation connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Verify Email Address



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/emailListValidation/latest/actions/verify-email-address?connectionId=$CONNECTION_ID&email=test%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "test@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/emailListValidation/latest/actions/verify-email-address?${params}`, {
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
      "result": "string"
    }
  ],
  "meta": {}
}
```

See the full [Verify Email Address action reference](actions/verify-email-address.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/emailListValidation/latest/actions/verify-email-address).
