# GrassBlade LRS: Delete Activity Profile

Deletes an activity profile from GrassBlade LRS.

```
DELETE https://connect.mindcloud.co/v1/universal/grassBladeLRS/latest/actions/delete-activity-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GrassBlade LRS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/grassBladeLRS/latest/actions/delete-activity-profile?connectionId=$CONNECTION_ID&activityId=https%3A%2F%2Fmindcloud.dev%2Fgrassblade%2Factivity%2Fstage3-20260406&profileId=mindcloud-activity-profile-stage3" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "activityId": "https://mindcloud.dev/grassblade/activity/stage3-20260406",
  "profileId": "mindcloud-activity-profile-stage3"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/grassBladeLRS/latest/actions/delete-activity-profile?${params}`, {
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
| `profileId` | string | yes | Example: `mindcloud-activity-profile-stage3`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native GrassBlade LRS API returns.

## Native endpoint

Through the native GrassBlade LRS API, this operation is `DELETE /activities/profile` (base URL `https://test.gblrs.com/xAPI`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-activity-profile.md) for the provider-specific parameters and requirements.

