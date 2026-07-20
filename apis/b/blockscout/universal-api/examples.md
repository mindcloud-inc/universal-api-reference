# Blockscout Universal API Examples

These examples use the MindCloud API key and Blockscout connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Address Counters

Retrieves activity counters for an address from Blockscout.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/blockscout/latest/actions/get-address-counters?connectionId=$CONNECTION_ID&address_hash_param=0xfFd12B32d000617551681973911Fd3ad49B89294" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "address_hash_param": "0xfFd12B32d000617551681973911Fd3ad49B89294"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/blockscout/latest/actions/get-address-counters?${params}`, {
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
      "token_transfers_count": 1,
      "transactions_count": 1,
      "validations_count": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Address Counters action reference](actions/get-address-counters.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/blockscout/latest/actions/get-address-counters).
