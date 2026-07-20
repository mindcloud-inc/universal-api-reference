# MailboxValidator Universal API Examples

These examples use the MindCloud API key and MailboxValidator connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Check Free Email Provider



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailboxValidator/latest/actions/check-free-email-provider?connectionId=$CONNECTION_ID&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailboxValidator/latest/actions/check-free-email-provider?${params}`, {
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
      "creditsAvailable": 1,
      "emailAddress": "ava@example.com",
      "isFree": true
    }
  ],
  "meta": {}
}
```

See the full [Check Free Email Provider action reference](actions/check-free-email-provider.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mailboxValidator/latest/actions/check-free-email-provider).
