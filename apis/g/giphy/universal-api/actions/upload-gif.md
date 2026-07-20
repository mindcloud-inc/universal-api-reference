# Giphy: Upload GIF

Uploads a GIF to Giphy.

```
POST https://connect.mindcloud.co/v1/universal/giphy/latest/actions/upload-gif
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Giphy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/giphy/latest/actions/upload-gif" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/giphy/latest/actions/upload-gif', {
  method: 'POST',
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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sourceImageUrl` | string | no |  |
| `file` | file | no |  |
| `tags` | string | no |  |
| `sourcePostUrl` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "meta": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `meta` | object |  |

## Native endpoint

Through the native Giphy API, this operation is `POST https://upload.giphy.com/v1/gifs` (base URL `https://api.giphy.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-gif.md) for the provider-specific parameters and requirements.

