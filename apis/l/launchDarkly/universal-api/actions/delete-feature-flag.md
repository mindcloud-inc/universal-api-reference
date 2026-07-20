# LaunchDarkly: Delete Feature Flag

Deletes an existing feature flag from LaunchDarkly.

```
DELETE https://connect.mindcloud.co/v1/universal/launchDarkly/latest/actions/delete-feature-flag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LaunchDarkly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/launchDarkly/latest/actions/delete-feature-flag?connectionId=$CONNECTION_ID&featureFlagKey=string&projectKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "featureFlagKey": "string",
  "projectKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/launchDarkly/latest/actions/delete-feature-flag?${params}`, {
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
| `featureFlagKey` | string | yes | The LaunchDarkly feature flag key. |
| `projectKey` | string | yes | The LaunchDarkly project key. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native LaunchDarkly API returns.

## Native endpoint

Through the native LaunchDarkly API, this operation is `DELETE /flags/:projectKey/:featureFlagKey` (base URL `https://app.launchdarkly.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-feature-flag.md) for the provider-specific parameters and requirements.

