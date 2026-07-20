# UK Bank Holidays Universal API Examples

These examples use the MindCloud API key and UK Bank Holidays connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Bank Holidays

Retrieves UK bank holiday dates from UK Bank Holidays.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uKBankHolidays/latest/actions/list-bank-holidays?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uKBankHolidays/latest/actions/list-bank-holidays?${params}`, {
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
      "bunting": true,
      "date": "string",
      "division": "string",
      "notes": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Bank Holidays action reference](actions/list-bank-holidays.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/uKBankHolidays/latest/actions/list-bank-holidays).
