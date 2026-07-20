# Lightfunnels Universal API Examples

These examples use the MindCloud API key and Lightfunnels connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Retrieve Account Pixels



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lightfunnels/latest/actions/retrieve-account-pixels?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lightfunnels/latest/actions/retrieve-account-pixels?${params}`, {
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
      "account": {
        "facebook_pixels": [
          {}
        ],
        "snapchat_pixels": [
          {}
        ],
        "tiktok_pixels": [
          {}
        ]
      }
    }
  ],
  "meta": {}
}
```

See the full [Retrieve Account Pixels action reference](actions/retrieve-account-pixels.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/lightfunnels/latest/actions/retrieve-account-pixels).

## Add Products to Store



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/lightfunnels/latest/actions/add-products-to-store" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lightfunnels/latest/actions/add-products-to-store', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
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
      "addProductsToStore": {
        "id": "string",
        "products": [
          {
            "id": "string"
          }
        ]
      }
    }
  ],
  "meta": {}
}
```

See the full [Add Products to Store action reference](actions/add-products-to-store.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/lightfunnels/latest/actions/add-products-to-store).
