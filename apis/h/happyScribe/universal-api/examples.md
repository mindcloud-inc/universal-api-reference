# HappyScribe Universal API Examples

These examples use the MindCloud API key and HappyScribe connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Signed URL

Retrieves a signed upload URL from HappyScribe.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/happyScribe/latest/actions/get-signed-url?connectionId=$CONNECTION_ID&filename=my_media.mp3" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "filename": "my_media.mp3"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/happyScribe/latest/actions/get-signed-url?${params}`, {
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
      "signedUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Get Signed URL action reference](actions/get-signed-url.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/happyScribe/latest/actions/get-signed-url).

## Confirm Order

Confirms an order in HappyScribe.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/happyScribe/latest/actions/confirm-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "49e1a97970944447b2dfe7ed5f00ce5a"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/happyScribe/latest/actions/confirm-order', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "49e1a97970944447b2dfe7ed5f00ce5a"
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
      "result": "string"
    }
  ],
  "meta": {}
}
```

See the full [Confirm Order action reference](actions/confirm-order.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/happyScribe/latest/actions/confirm-order).
