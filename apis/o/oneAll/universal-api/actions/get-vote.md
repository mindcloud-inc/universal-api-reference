# OneAll: Get Vote

Retrieves a LoudVoice vote from OneAll.

```
GET https://connect.mindcloud.co/v1/universal/oneAll/latest/actions/get-vote
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OneAll `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneAll/latest/actions/get-vote?connectionId=$CONNECTION_ID&authorToken=string&commentToken=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "authorToken": "string",
  "commentToken": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oneAll/latest/actions/get-vote?${params}`, {
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
| `authorToken` | string | yes | The OneAll author token. |
| `commentToken` | string | yes | The OneAll comment token. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native OneAll API returns.

## Native endpoint

Through the native OneAll API, this operation is `GET /loudvoice/votes/comments/<comment_token>/authors/<author_token>.json` (base URL `https://mindcloudco.api.oneall.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-vote.md) for the provider-specific parameters and requirements.

