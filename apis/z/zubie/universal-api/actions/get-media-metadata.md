# Zubie: Get Media Metadata

Retrieves media metadata from Zubie.

```
GET https://connect.mindcloud.co/v1/universal/zubie/latest/actions/get-media-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zubie `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zubie/latest/actions/get-media-metadata?connectionId=$CONNECTION_ID&media_key=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "media_key": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zubie/latest/actions/get-media-metadata?${params}`, {
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
| `media_key` | string | yes | Unique media entity key. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "key": "string",
      "labels": "string",
      "media_type": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `key` | string |  |
| `labels` | string |  |
| `media_type` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Zubie API, this operation is `GET /media/{media_key}` (base URL `https://api.zubiecar.com/api/v2/zinc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-media-metadata.md) for the provider-specific parameters and requirements.

