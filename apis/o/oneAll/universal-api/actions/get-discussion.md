# OneAll: Get Discussion

Retrieves LoudVoice discussion details from OneAll.

```
GET https://connect.mindcloud.co/v1/universal/oneAll/latest/actions/get-discussion
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OneAll `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneAll/latest/actions/get-discussion?connectionId=$CONNECTION_ID&discussionToken=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "discussionToken": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oneAll/latest/actions/get-discussion?${params}`, {
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
| `discussionToken` | string | yes | The OneAll discussion token. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native OneAll API returns.

## Native endpoint

Through the native OneAll API, this operation is `GET /loudvoice/discussions/<discussion_token>.json` (base URL `https://mindcloudco.api.oneall.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-discussion.md) for the provider-specific parameters and requirements.

