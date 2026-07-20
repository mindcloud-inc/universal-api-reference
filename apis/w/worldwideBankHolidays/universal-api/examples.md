# Worldwide Bank Holidays Universal API Examples

These examples use the MindCloud API key and Worldwide Bank Holidays connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Check Today Public Holiday



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/worldwideBankHolidays/latest/actions/check-today-public-holiday?connectionId=$CONNECTION_ID&countryCode=US" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "countryCode": "US"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/worldwideBankHolidays/latest/actions/check-today-public-holiday?${params}`, {
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
      "status": 1
    }
  ],
  "meta": {}
}
```

See the full [Check Today Public Holiday action reference](actions/check-today-public-holiday.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/worldwideBankHolidays/latest/actions/check-today-public-holiday).
