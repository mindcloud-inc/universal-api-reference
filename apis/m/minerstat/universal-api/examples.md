# Minerstat Universal API Examples

These examples use the MindCloud API key and Minerstat connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Coins

Retrieves coins from the Minerstat catalog.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/minerstat/latest/actions/list-coins?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/minerstat/latest/actions/list-coins?${params}`, {
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
      "algorithm": "string",
      "coin": "string",
      "difficulty": 1,
      "id": "string",
      "name": "Ava Chen",
      "network_hashrate": 1,
      "price": 1,
      "reward": 1,
      "reward_block": 1,
      "reward_unit": "string",
      "type": "string",
      "updated": 1,
      "volume": 1
    }
  ],
  "meta": {}
}
```

See the full [List Coins action reference](actions/list-coins.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/minerstat/latest/actions/list-coins).
