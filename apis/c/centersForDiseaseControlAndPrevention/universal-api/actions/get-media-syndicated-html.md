# Centers for Disease Control and Prevention: Get Media Syndicated HTML

Retrieves syndicated HTML for media from CDC Content Services.

```
GET https://connect.mindcloud.co/v1/universal/centersForDiseaseControlAndPrevention/latest/actions/get-media-syndicated-html
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Centers for Disease Control and Prevention `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/centersForDiseaseControlAndPrevention/latest/actions/get-media-syndicated-html?connectionId=$CONNECTION_ID&mediaId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "mediaId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/centersForDiseaseControlAndPrevention/latest/actions/get-media-syndicated-html?${params}`, {
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
| `cssClasses` | string | no | Comma-delimited class IDs to retrieve from the source page. |
| `mediaId` | number | yes | The identifier of the media. |
| `stripScripts` | boolean | no | When true, JavaScript is stripped from the syndicated content. Default: `true`. |
| `stripAnchors` | boolean | no | When true, anchor tags are stripped from the syndicated content. Default: `false`. |
| `stripImages` | boolean | no | When true, images are stripped from the syndicated content. Default: `false`. |

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
| `content` | string |  |
| `description` | string |  |
| `mediaId` | number |  |
| `mediaType` | string |  |
| `name` | string |  |
| `sourceUrl` | string |  |
| `targetUrl` | string |  |

## Native endpoint

Through the native Centers for Disease Control and Prevention API, this operation is `GET /v2/resources/media/:mediaId/syndicate` (base URL `https://tools.cdc.gov/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-media-syndicated-html.md) for the provider-specific parameters and requirements.

