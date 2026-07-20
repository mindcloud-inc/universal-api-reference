# Seqera: Update Workspace Participant Role

Updates a workspace participant role in Seqera.

```
PUT https://connect.mindcloud.co/v1/universal/seqera/latest/actions/update-workspace-participant-role
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Seqera `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/seqera/latest/actions/update-workspace-participant-role" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "orgId": 1,
  "participantId": 1,
  "workspaceId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/seqera/latest/actions/update-workspace-participant-role', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "orgId": 1,
    "participantId": 1,
    "workspaceId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `orgId` | number | yes |  |
| `participantId` | number | yes |  |
| `role` | string | no |  |
| `workspaceId` | number | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Seqera API returns.

## Native endpoint

Through the native Seqera API, this operation is `PUT /orgs/:orgId/workspaces/:workspaceId/participants/:participantId/role` (base URL `https://api.cloud.seqera.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-workspace-participant-role.md) for the provider-specific parameters and requirements.

