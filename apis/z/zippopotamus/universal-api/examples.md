# Zippopotamus Universal API Examples

These examples use the MindCloud API key and Zippopotamus connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Nearby Places by Postal Code

Retrieves nearby places in Zippopotamus by postal code.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zippopotamus/latest/actions/list-nearby-places-by-postal-code?connectionId=$CONNECTION_ID&country=US&postalcode=90210" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "country": "US",
  "postalcode": "90210"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zippopotamus/latest/actions/list-nearby-places-by-postal-code?${params}`, {
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
      "near latitude": 1,
      "near longitude": 1,
      "nearby": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Nearby Places by Postal Code action reference](actions/list-nearby-places-by-postal-code.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zippopotamus/latest/actions/list-nearby-places-by-postal-code).
