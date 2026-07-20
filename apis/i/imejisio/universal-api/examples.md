# Imejis.io Universal API Examples

These examples use the MindCloud API key and Imejis.io connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Render Image

Creates a rendered image in Imejis.io by design ID.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/imejisio/latest/actions/render-image" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "designId": "HxQGYmW6hKu-HAORyRazt"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/imejisio/latest/actions/render-image', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "designId": "HxQGYmW6hKu-HAORyRazt"
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

See the full [Render Image action reference](actions/render-image.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/imejisio/latest/actions/render-image).
