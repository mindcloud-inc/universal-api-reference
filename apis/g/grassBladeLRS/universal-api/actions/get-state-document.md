# GrassBlade LRS: Get State Document

Retrieves a state document from GrassBlade LRS.

```
GET https://connect.mindcloud.co/v1/universal/grassBladeLRS/latest/actions/get-state-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GrassBlade LRS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/grassBladeLRS/latest/actions/get-state-document?connectionId=$CONNECTION_ID&activityId=https%3A%2F%2Fmindcloud.dev%2Fgrassblade%2Factivity%2Fstage3-20260406&agent=%5Bobject%20Object%5D&stateId=mindcloud-state-stage3" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "activityId": "https://mindcloud.dev/grassblade/activity/stage3-20260406",
  "agent": "[object Object]",
  "stateId": "mindcloud-state-stage3"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/grassBladeLRS/latest/actions/get-state-document?${params}`, {
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
| `stateId` | string | yes | Example: `mindcloud-state-stage3`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `registration` | string | no | Example: `7d1e5c30-1a57-4b72-bf87-23e7fd355f90`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native GrassBlade LRS API returns.

## Native endpoint

Through the native GrassBlade LRS API, this operation is `GET /activities/state` (base URL `https://test.gblrs.com/xAPI`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-state-document.md) for the provider-specific parameters and requirements.

