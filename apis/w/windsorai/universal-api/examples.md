# Windsor.ai Universal API Examples

These examples use the MindCloud API key and Windsor.ai connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Co-User Linked Accounts

Retrieves co-user linked accounts from Windsor.ai.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/windsorai/latest/actions/list-co-user-linked-accounts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/windsorai/latest/actions/list-co-user-linked-accounts?${params}`, {
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

See the full [List Co-User Linked Accounts action reference](actions/list-co-user-linked-accounts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/windsorai/latest/actions/list-co-user-linked-accounts).
