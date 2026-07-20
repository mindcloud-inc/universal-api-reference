# BackgroundCut Universal API Examples

These examples use the MindCloud API key and BackgroundCut connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Generate Alpha Mask From Base64 (v2)

Generates an alpha mask in BackgroundCut from a base64 image.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/backgroundCut/latest/actions/generate-alpha-mask-from-base64-v2" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "imageFileB64": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/backgroundCut/latest/actions/generate-alpha-mask-from-base64-v2', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "imageFileB64": "string"
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
      "data": [
        1
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Generate Alpha Mask From Base64 (v2) action reference](actions/generate-alpha-mask-from-base64-v2.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/backgroundCut/latest/actions/generate-alpha-mask-from-base64-v2).
