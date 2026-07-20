# Picsart Universal API Examples

These examples use the MindCloud API key and Picsart connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Credits Balance

Retrieves your remaining Picsart credits balance.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/picsart/latest/actions/get-credits-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/picsart/latest/actions/get-credits-balance?${params}`, {
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
      "credits": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Credits Balance action reference](actions/get-credits-balance.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/picsart/latest/actions/get-credits-balance).

## Adjust Image

Creates an adjusted image in Picsart.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/picsart/latest/actions/adjust-image" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "imageUrl": "https://pastatic.picsart.com/31399405932227146498.png"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/picsart/latest/actions/adjust-image', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "imageUrl": "https://pastatic.picsart.com/31399405932227146498.png"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "id": "string",
        "url": "https://example.com"
      },
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Adjust Image action reference](actions/adjust-image.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/picsart/latest/actions/adjust-image).
