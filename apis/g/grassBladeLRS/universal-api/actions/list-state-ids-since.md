# GrassBlade LRS: List State IDs Since

Retrieves state document IDs from GrassBlade LRS since a timestamp.

```
GET https://connect.mindcloud.co/v1/universal/grassBladeLRS/latest/actions/list-state-ids-since
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GrassBlade LRS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/grassBladeLRS/latest/actions/list-state-ids-since?connectionId=$CONNECTION_ID&activityId=https%3A%2F%2Fmindcloud.dev%2Fgrassblade%2Factivity%2Fstage3-20260406&agent=%5Bobject%20Object%5D&since=2026-04-06T18%3A05%3A00Z" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "activityId": "https://mindcloud.dev/grassblade/activity/stage3-20260406",
  "agent": "[object Object]",
  "since": "2026-04-06T18:05:00Z"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/grassBladeLRS/latest/actions/list-state-ids-since?${params}`, {
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
| `since` | string | yes | Example: `2026-04-06T18:05:00Z`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native GrassBlade LRS API returns.

## Native endpoint

Through the native GrassBlade LRS API, this operation is `GET /activities/state` (base URL `https://test.gblrs.com/xAPI`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-state-ids-since.md) for the provider-specific parameters and requirements.

