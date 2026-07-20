# Cloudmersive Video and Media: Convert Audio to MP3

Converts an audio file to MP3 in Cloudmersive Video and Media.

```
GET https://connect.mindcloud.co/v1/universal/cloudmersiveVideoAndMedia/latest/actions/convert-audio-to-mp3
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudmersive Video and Media `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudmersiveVideoAndMedia/latest/actions/convert-audio-to-mp3?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudmersiveVideoAndMedia/latest/actions/convert-audio-to-mp3?${params}`, {
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
| `fileUrl` | string | no | URL of an audio file to convert. Cloudmersive recommends this option for files larger than 2GB. |
| `inputFile` | file | no | Input audio file to convert. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `bitRate` | number | no | Desired bitrate in kilobytes per second (48 to 1411). |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Cloudmersive Video and Media API returns.

## Native endpoint

Through the native Cloudmersive Video and Media API, this operation is `POST /video/convert/to/mp3` (base URL `https://api.cloudmersive.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert-audio-to-mp3.md) for the provider-specific parameters and requirements.

