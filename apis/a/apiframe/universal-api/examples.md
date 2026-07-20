# Apiframe Universal API Examples

These examples use the MindCloud API key and Apiframe connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account Info

Retrieves your Apiframe account details and credits.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/apiframe/latest/actions/get-account-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/apiframe/latest/actions/get-account-info?${params}`, {
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
      "credits": 1,
      "email": "ava@example.com",
      "next_billing_date": "string",
      "plan": "string",
      "subscription_credits": 1,
      "topup_credits": 1,
      "total_images": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Account Info action reference](actions/get-account-info.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/apiframe/latest/actions/get-account-info).

## Blend Images

Creates an image blending task in Apiframe.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/apiframe/latest/actions/blend-images" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "imageUrls[]": [
    "https://example.com"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/apiframe/latest/actions/blend-images', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "imageUrls[]": ["https://example.com"]
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
      "task_id": "string"
    }
  ],
  "meta": {}
}
```

See the full [Blend Images action reference](actions/blend-images.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/apiframe/latest/actions/blend-images).
