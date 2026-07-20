# SqlBak Universal API Examples

These examples use the MindCloud API key and SqlBak connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account Information

Retrieves account information from SqlBak.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sqlBak/latest/actions/get-account-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sqlBak/latest/actions/get-account-information?${params}`, {
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
      "company": "string",
      "created_at": 1,
      "credit_usd": 1,
      "email": "ava@example.com",
      "entity": "string",
      "is_suspended": true,
      "managed_accounts": [
        {}
      ],
      "manager_accounts": [
        {}
      ],
      "name": "Ava Chen",
      "subscription": {}
    }
  ],
  "meta": {}
}
```

See the full [Get Account Information action reference](actions/get-account-information.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sqlBak/latest/actions/get-account-information).
