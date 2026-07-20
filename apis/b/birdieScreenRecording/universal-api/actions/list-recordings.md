# Birdie Screen Recording: List Recordings

Retrieves recordings from Birdie Screen Recording.

```
GET https://connect.mindcloud.co/v1/universal/birdieScreenRecording/latest/actions/list-recordings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Birdie Screen Recording `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/birdieScreenRecording/latest/actions/list-recordings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/birdieScreenRecording/latest/actions/list-recordings?${params}`, {
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
| `ticket` | string | no | Filter recordings by ticket id. |
| `email` | string | no | Filter recordings by customer email. |
| `param` | string | no | Filter recordings by a metadata key added to the recording link. |
| `value` | string | no | Metadata value to match for the selected metadata key. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Birdie Screen Recording API returns.

## Native endpoint

Through the native Birdie Screen Recording API, this operation is `GET /api/v1/videos` (base URL `https://app.birdie.so`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-recordings.md) for the provider-specific parameters and requirements.

