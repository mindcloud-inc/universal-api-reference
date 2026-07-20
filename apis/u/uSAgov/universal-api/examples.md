# USA.gov Universal API Examples

These examples use the MindCloud API key and USA.gov connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Download English Site Live Pages

Downloads live English site pages visited on USA.gov.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uSAgov/latest/actions/get-usagov-all-pages-people-are-visiting-csv?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uSAgov/latest/actions/get-usagov-all-pages-people-are-visiting-csv?${params}`, {
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
      "response": "string"
    }
  ],
  "meta": {}
}
```

See the full [Download English Site Live Pages action reference](actions/get-usagov-all-pages-people-are-visiting-csv.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/uSAgov/latest/actions/get-usagov-all-pages-people-are-visiting-csv).
