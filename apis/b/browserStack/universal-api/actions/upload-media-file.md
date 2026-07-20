# BrowserStack: Upload Media File

Uploads a media file to BrowserStack Automate.

```
POST https://connect.mindcloud.co/v1/universal/browserStack/latest/actions/upload-media-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BrowserStack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/browserStack/latest/actions/upload-media-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/browserStack/latest/actions/upload-media-file', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file` | file | yes | Public URL or base64 content for the media file to upload. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native BrowserStack API returns.

## Native endpoint

Through the native BrowserStack API, this operation is `POST https://api-cloud.browserstack.com/automate/upload-media` (base URL `https://api.browserstack.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-media-file.md) for the provider-specific parameters and requirements.

