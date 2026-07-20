# CDC Content Services: Get Media Syndication

Retrieves media syndication details from CDC Content Services.

```
GET https://connect.mindcloud.co/v1/universal/cDCContentServices/latest/actions/get-media-syndication
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CDC Content Services `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cDCContentServices/latest/actions/get-media-syndication?connectionId=$CONNECTION_ID&mediaId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "mediaId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cDCContentServices/latest/actions/get-media-syndication?${params}`, {
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
| `mediaId` | number | yes | CDC media identifier. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `stripScripts` | boolean | no | When true, JavaScript is stripped from syndicated results. CDC defaults to true. |
| `stripImages` | boolean | no | When true, images are stripped from syndicated results. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": "string",
      "description": "string",
      "mediaId": 1,
      "mediaType": "string",
      "name": "Ava Chen",
      "sourceUrl": "https://example.com",
      "targetUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | string | Syndicated HTML/content. |
| `description` | string | Content description. |
| `mediaId` | number | CDC media identifier. |
| `mediaType` | string | CDC media type. |
| `name` | string | Content title/name. |
| `sourceUrl` | string | Original CDC source URL. |
| `targetUrl` | string | Target URL. |

## Native endpoint

Through the native CDC Content Services API, this operation is `GET /v2/resources/media/[:mediaId]/syndicate` (base URL `https://tools.cdc.gov/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-media-syndication.md) for the provider-specific parameters and requirements.

