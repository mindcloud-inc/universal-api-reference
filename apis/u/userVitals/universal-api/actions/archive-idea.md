# UserVitals: Archive Idea

Archives an idea in the roadmap API.

```
DELETE https://connect.mindcloud.co/v1/universal/userVitals/latest/actions/archive-idea
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UserVitals `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/userVitals/latest/actions/archive-idea?connectionId=$CONNECTION_ID&publicItemTokenId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "publicItemTokenId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/userVitals/latest/actions/archive-idea?${params}`, {
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
| `publicItemTokenId` | string | yes | The Base64-encoded public item token id. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native UserVitals API returns.

## Native endpoint

Through the native UserVitals API, this operation is `DELETE /ideas/:publicItemTokenId` (base URL `https://app.roadmap.space/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/archive-idea.md) for the provider-specific parameters and requirements.

