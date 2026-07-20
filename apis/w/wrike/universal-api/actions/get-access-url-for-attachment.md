# Wrike: Get Access URL for Attachment

Retrieves an access URL for a Wrike attachment.

```
GET https://connect.mindcloud.co/v1/universal/wrike/latest/actions/get-access-url-for-attachment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wrike `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wrike/latest/actions/get-access-url-for-attachment?connectionId=$CONNECTION_ID&attachmentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "attachmentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wrike/latest/actions/get-access-url-for-attachment?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `attachmentId` | string | yes | Wrike attachment ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "playlistUrl": "https://example.com",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `playlistUrl` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Wrike API, this operation is `GET /attachments/:attachmentId/url` (base URL `https://{{credentials.accessTokenRequest.host}}/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-access-url-for-attachment.md) for the provider-specific parameters and requirements.

