# CoinCap Universal API Examples

These examples use the MindCloud API key and CoinCap connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Assets

Retrieves assets from CoinCap.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coinCap/latest/actions/list-assets?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coinCap/latest/actions/list-assets?${params}`, {
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
      "changePercent24Hr": "string",
      "explorer": "string",
      "id": "string",
      "marketCapUsd": "string",
      "maxSupply": "string",
      "name": "Ava Chen",
      "priceUsd": "string",
      "rank": "string",
      "supply": "string",
      "symbol": "string",
      "tokens": {},
      "volumeUsd24Hr": "string",
      "vwap24Hr": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Assets action reference](actions/list-assets.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/coinCap/latest/actions/list-assets).
