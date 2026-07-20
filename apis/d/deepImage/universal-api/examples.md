# DeepImage Universal API Examples

These examples use the MindCloud API key and DeepImage connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account Info

Retrieves your account information from DeepImage.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deepImage/latest/actions/get-account-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deepImage/latest/actions/get-account-info?${params}`, {
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
  "data": [],
  "meta": {}
}
```

See the full [Get Account Info action reference](actions/get-account-info.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/deepImage/latest/actions/get-account-info).

## Accurate Business Avatar

Creates an accurate business avatar in DeepImage.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/deepImage/latest/actions/accurate-business-avatar" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://deep-image.ai/api-example3.jpg",
  "background.generate.description": "A woman sitting behind a desk in a modern office environment. Her smiling face is seen from behind her computer screen, with only the top of her head and a portion of her shoulders visible. The office space around her is bright and airy, illuminated by soft, natural light streaming in from large windows."
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/deepImage/latest/actions/accurate-business-avatar', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://deep-image.ai/api-example3.jpg",
    "background.generate.description": "A woman sitting behind a desk in a modern office environment. Her smiling face is seen from behind her computer screen, with only the top of her head and a portion of her shoulders visible. The office space around her is bright and airy, illuminated by soft, natural light streaming in from large windows."
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
      "imageApp": {},
      "job": "string",
      "originalImg": "string",
      "queue": 1
    }
  ],
  "meta": {}
}
```

See the full [Accurate Business Avatar action reference](actions/accurate-business-avatar.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/deepImage/latest/actions/accurate-business-avatar).
