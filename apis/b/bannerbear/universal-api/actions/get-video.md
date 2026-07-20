# Bannerbear: Get Video

Retrieves video from Bannerbear.

```
GET https://connect.mindcloud.co/v1/universal/bannerbear/latest/actions/get-video
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bannerbear `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bannerbear/latest/actions/get-video?connectionId=$CONNECTION_ID&uid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bannerbear/latest/actions/get-video?${params}`, {
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
| `uid` | string | yes | The unique ID of the video to retrieve. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bannerbear API returns.

## Native endpoint

Through the native Bannerbear API, this operation is `GET /v2/videos/:uid` (base URL `https://api.bannerbear.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-video.md) for the provider-specific parameters and requirements.

