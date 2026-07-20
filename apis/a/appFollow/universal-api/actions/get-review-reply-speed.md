# AppFollow: Get Review Reply Speed

Retrieves review reply speed statistics from AppFollow.

```
GET https://connect.mindcloud.co/v1/universal/appFollow/latest/actions/get-review-reply-speed
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AppFollow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/appFollow/latest/actions/get-review-reply-speed?connectionId=$CONNECTION_ID&extId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "extId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/appFollow/latest/actions/get-review-reply-speed?${params}`, {
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
| `extId` | string | yes | App external ID. |
| `answerUserId` | string | no | User ID. |
| `date` | string | no | Reviews date. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native AppFollow API returns.

## Native endpoint

Through the native AppFollow API, this operation is `GET /api/v2/reviews/stats/replies/speed` (base URL `https://api.appfollow.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-review-reply-speed.md) for the provider-specific parameters and requirements.

