# AddressZen Universal API Examples

These examples use the MindCloud API key and AddressZen connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Email Validation

Retrieves email validation details from AddressZen.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/addressZen/latest/actions/email-validation?connectionId=$CONNECTION_ID&query=test%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "test@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/addressZen/latest/actions/email-validation?${params}`, {
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
      "catchall": true,
      "deliverable": true,
      "disposable": true,
      "free": true,
      "result": "string",
      "role": true,
      "suggestions": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

See the full [Email Validation action reference](actions/email-validation.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/addressZen/latest/actions/email-validation).
