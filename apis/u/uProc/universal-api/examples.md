# UProc Universal API Examples

These examples use the MindCloud API key and UProc connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Check Credit Card Checksum



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uProc/latest/actions/check-credit-card-checksum?connectionId=$CONNECTION_ID&credit_card=4024007151839544" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "credit_card": "4024007151839544"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uProc/latest/actions/check-credit-card-checksum?${params}`, {
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
      "balance": 1,
      "criteria": "string",
      "error": true,
      "message": {},
      "normalized": true,
      "params": {},
      "price": 1,
      "processor": "string",
      "realPrice": 1,
      "result": true,
      "time": 1,
      "totalRows": 1
    }
  ],
  "meta": {}
}
```

See the full [Check Credit Card Checksum action reference](actions/check-credit-card-checksum.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/uProc/latest/actions/check-credit-card-checksum).
