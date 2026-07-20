# Restream: Get Clip Download URL

Generates a download URL for a clip in Restream.

```
GET https://connect.mindcloud.co/v1/universal/restream/latest/actions/get-clip-download-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Restream `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/restream/latest/actions/get-clip-download-url?connectionId=$CONNECTION_ID&clipId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "clipId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/restream/latest/actions/get-clip-download-url?${params}`, {
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
| `clipId` | string | yes | The ID of the clip whose download URL to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "downloadUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `downloadUrl` | string |  |

## Native endpoint

Through the native Restream API, this operation is `GET /user/clips/:clipId/download` (base URL `https://api.restream.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-clip-download-url.md) for the provider-specific parameters and requirements.

