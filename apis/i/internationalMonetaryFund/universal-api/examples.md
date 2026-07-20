# International Monetary Fund Universal API Examples

These examples use the MindCloud API key and International Monetary Fund connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Indicators

Retrieves available indicators from the IMF DataMapper API.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/internationalMonetaryFund/latest/actions/list-indicators?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/internationalMonetaryFund/latest/actions/list-indicators?${params}`, {
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
      "dataset": "string",
      "description": "string",
      "id": "string",
      "label": "string",
      "source": "string",
      "unit": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Indicators action reference](actions/list-indicators.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/internationalMonetaryFund/latest/actions/list-indicators).
