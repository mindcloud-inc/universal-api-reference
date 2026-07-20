# GrassBlade LRS: Delete Agent Profile

Deletes an agent profile from GrassBlade LRS.

```
DELETE https://connect.mindcloud.co/v1/universal/grassBladeLRS/latest/actions/delete-agent-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GrassBlade LRS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/grassBladeLRS/latest/actions/delete-agent-profile?connectionId=$CONNECTION_ID&agent=%5Bobject%20Object%5D&profileId=mindcloud-agent-profile-stage3" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "agent": "[object Object]",
  "profileId": "mindcloud-agent-profile-stage3"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/grassBladeLRS/latest/actions/delete-agent-profile?${params}`, {
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
| `agent` | string | yes | Example: `[object Object]`. |
| `profileId` | string | yes | Example: `mindcloud-agent-profile-stage3`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native GrassBlade LRS API returns.

## Native endpoint

Through the native GrassBlade LRS API, this operation is `DELETE /agents/profile` (base URL `https://test.gblrs.com/xAPI`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-agent-profile.md) for the provider-specific parameters and requirements.

