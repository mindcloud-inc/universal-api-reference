# Reka Vision Universal API Examples

These examples use the MindCloud API key and Reka Vision connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Feature Catalog (V2)

Retrieves the feature catalog from Reka Vision.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rekaVision/latest/actions/get-feature-catalog-v2?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rekaVision/latest/actions/get-feature-catalog-v2?${params}`, {
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
      "dependsOn": [
        "string"
      ],
      "description": "string",
      "name": "Ava Chen",
      "note": "string",
      "produces": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

See the full [Get Feature Catalog (V2) action reference](actions/get-feature-catalog-v2.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/rekaVision/latest/actions/get-feature-catalog-v2).

## Create Reel (V1)

Creates highlight reels in Reka Vision.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rekaVision/latest/actions/create-reel-v1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "videoUrls[]": [
    "https://example.com"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rekaVision/latest/actions/create-reel-v1', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "videoUrls[]": ["https://example.com"]
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
      "value": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Reel (V1) action reference](actions/create-reel-v1.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/rekaVision/latest/actions/create-reel-v1).
