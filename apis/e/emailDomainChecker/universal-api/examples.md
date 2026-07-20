# Email Domain Checker Universal API Examples

These examples use the MindCloud API key and Email Domain Checker connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Check Domain



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/emailDomainChecker/latest/actions/check-domain?connectionId=$CONNECTION_ID&domain=mightora.io" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domain": "mightora.io"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/emailDomainChecker/latest/actions/check-domain?${params}`, {
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
      "email_delivered_to": "ava@example.com",
      "email_delivered_to_array": [
        "ava@example.com"
      ],
      "message": "string",
      "message_from_developer": "string",
      "more_info": "https://example.com",
      "valid_email_domain": true
    }
  ],
  "meta": {}
}
```

See the full [Check Domain action reference](actions/check-domain.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/emailDomainChecker/latest/actions/check-domain).
