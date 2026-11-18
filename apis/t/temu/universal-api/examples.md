# Temu Universal API Examples

These examples use the MindCloud API key and Temu connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Combined Shipping Groups

Retrieve combined shipping groups including lists of parent orders that can be combined for shipping.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/temu/latest/actions/get-combined-shipping-groups?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/temu/latest/actions/get-combined-shipping-groups?${params}`, {
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

See the full [Get Combined Shipping Groups action reference](actions/get-combined-shipping-groups.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/temu/latest/actions/get-combined-shipping-groups).
