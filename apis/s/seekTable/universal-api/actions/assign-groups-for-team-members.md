# SeekTable: Assign Groups For Team Members

Assigns team groups to SeekTable team members.

```
PUT https://connect.mindcloud.co/v1/universal/seekTable/latest/actions/assign-groups-for-team-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SeekTable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/seekTable/latest/actions/assign-groups-for-team-members" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "1",
  "assignments[]": [
    {}
  ],
  "assignments[].email": "ava@example.com",
  "assignments[].groupIds[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/seekTable/latest/actions/assign-groups-for-team-members', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "1",
    "assignments[]": [{}],
    "assignments[].email": "ava@example.com",
    "assignments[].groupIds[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | ID of the user account that owns the team. Example: `1`. |
| `assignments[]` | array<object> | yes | Team-member group assignments to apply in one request. |
| `assignments[].email` | string | yes | Login email of the team member to update. |
| `assignments[].groupIds[]` | array<string> | yes | IDs of the team groups that should be assigned to this member. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SeekTable API returns.

## Native endpoint

Through the native SeekTable API, this operation is `POST /api/account/:id/team/member/assigngroups` (base URL `https://www.seektable.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/assign-groups-for-team-members.md) for the provider-specific parameters and requirements.

