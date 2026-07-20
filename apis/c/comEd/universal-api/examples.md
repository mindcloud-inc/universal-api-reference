# ComEd Universal API Examples

These examples use the MindCloud API key and ComEd connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current Hour Average

Retrieves the current hour average price from ComEd.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/comEd/latest/actions/get-current-hour-average?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/comEd/latest/actions/get-current-hour-average?${params}`, {
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
      "millisUTC": "string",
      "price": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Current Hour Average action reference](actions/get-current-hour-average.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/comEd/latest/actions/get-current-hour-average).
