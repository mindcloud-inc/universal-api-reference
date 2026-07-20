# Pinghome: Delete Oncall Schedule

Deletes an existing on-call schedule from Pinghome.

```
DELETE https://connect.mindcloud.co/v1/universal/pinghome/latest/actions/delete-oncall-schedule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pinghome `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/pinghome/latest/actions/delete-oncall-schedule?connectionId=$CONNECTION_ID&teamId=string&teamMemberId=string&createdAt=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "teamId": "string",
  "teamMemberId": "string",
  "createdAt": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pinghome/latest/actions/delete-oncall-schedule?${params}`, {
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
| `teamId` | string | yes | The unique ID of the team. |
| `teamMemberId` | string | yes | The unique ID of the team member whose schedule is being deleted. |
| `createdAt` | string | yes | The creation timestamp identifying the schedule. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Pinghome API returns.

## Native endpoint

Through the native Pinghome API, this operation is `DELETE /incident-cmd/v1/team/:id/schedule` (base URL `https://api.pinghome.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-oncall-schedule.md) for the provider-specific parameters and requirements.

