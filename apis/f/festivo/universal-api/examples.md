# Festivo Universal API Examples

These examples use the MindCloud API key and Festivo connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Available Countries

Retrieves available country codes from Festivo.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/festivo/latest/actions/list-available-countries?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/festivo/latest/actions/list-available-countries?${params}`, {
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
      "code": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Available Countries action reference](actions/list-available-countries.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/festivo/latest/actions/list-available-countries).
