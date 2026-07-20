# Crossmint Universal API Examples

These examples use the MindCloud API key and Crossmint connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Usage

Retrieves project usage data from Crossmint.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/crossmint/latest/actions/get-usage?connectionId=$CONNECTION_ID&startDate=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "startDate": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/crossmint/latest/actions/get-usage?${params}`, {
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
      "data": [
        {
          "dimension": "string",
          "usage": [
            {
              "activeWallets": 1,
              "month": "string"
            }
          ]
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [Get Usage action reference](actions/get-usage.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/crossmint/latest/actions/get-usage).

## Create Collection

Creates a collection in Crossmint.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/crossmint/latest/actions/create-collection" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "chain": "base-sepolia",
  "metadata.name": "MindCloud Test Collection",
  "metadata.description": "Collection created by MindCloud for Crossmint runtime testing.",
  "metadata.imageUrl": "https://www.crossmint.com/assets/crossmint/logo.png",
  "metadata.symbol": "MCTEST",
  "fungibility": "non-fungible"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/crossmint/latest/actions/create-collection', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "chain": "base-sepolia",
    "metadata.name": "MindCloud Test Collection",
    "metadata.description": "Collection created by MindCloud for Crossmint runtime testing.",
    "metadata.imageUrl": "https://www.crossmint.com/assets/crossmint/logo.png",
    "metadata.symbol": "MCTEST",
    "fungibility": "non-fungible"
  })
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

See the full [Create Collection action reference](actions/create-collection.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/crossmint/latest/actions/create-collection).
