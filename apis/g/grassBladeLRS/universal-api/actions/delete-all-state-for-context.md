# GrassBlade LRS: Delete All State For Context

Deletes all state documents for a context in GrassBlade LRS.

```
DELETE https://connect.mindcloud.co/v1/universal/grassBladeLRS/latest/actions/delete-all-state-for-context
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GrassBlade LRS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/grassBladeLRS/latest/actions/delete-all-state-for-context?connectionId=$CONNECTION_ID&activityId=https%3A%2F%2Fmindcloud.dev%2Fgrassblade%2Factivity%2Fstage3-20260406&agent=%5Bobject%20Object%5D&registration=7d1e5c30-1a57-4b72-bf87-23e7fd355f90" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "activityId": "https://mindcloud.dev/grassblade/activity/stage3-20260406",
  "agent": "[object Object]",
  "registration": "7d1e5c30-1a57-4b72-bf87-23e7fd355f90"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/grassBladeLRS/latest/actions/delete-all-state-for-context?${params}`, {
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
| `activityId` | string | yes | Example: `https://mindcloud.dev/grassblade/activity/stage3-20260406`. |
| `agent` | string | yes | Example: `[object Object]`. |
| `registration` | string | yes | Example: `7d1e5c30-1a57-4b72-bf87-23e7fd355f90`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native GrassBlade LRS API returns.

## Native endpoint

Through the native GrassBlade LRS API, this operation is `DELETE /activities/state` (base URL `https://test.gblrs.com/xAPI`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-all-state-for-context.md) for the provider-specific parameters and requirements.

