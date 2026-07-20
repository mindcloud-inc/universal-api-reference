# LaunchDarkly: Delete Segment

Deletes an existing segment from LaunchDarkly.

```
DELETE https://connect.mindcloud.co/v1/universal/launchDarkly/latest/actions/delete-segment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LaunchDarkly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/launchDarkly/latest/actions/delete-segment?connectionId=$CONNECTION_ID&environmentKey=string&projectKey=string&segmentKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "environmentKey": "string",
  "projectKey": "string",
  "segmentKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/launchDarkly/latest/actions/delete-segment?${params}`, {
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
| `environmentKey` | string | yes | The LaunchDarkly environment key. |
| `projectKey` | string | yes | The LaunchDarkly project key. |
| `segmentKey` | string | yes | The LaunchDarkly segment key. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native LaunchDarkly API returns.

## Native endpoint

Through the native LaunchDarkly API, this operation is `DELETE /segments/:projectKey/:environmentKey/:segmentKey` (base URL `https://app.launchdarkly.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-segment.md) for the provider-specific parameters and requirements.

