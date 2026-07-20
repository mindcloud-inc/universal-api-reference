# Seqera: List Workspace Participants

Retrieves workspace participants from Seqera.

```
GET https://connect.mindcloud.co/v1/universal/seqera/latest/actions/list-workspace-participants
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Seqera `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seqera/latest/actions/list-workspace-participants?connectionId=$CONNECTION_ID&orgId=1&workspaceId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "orgId": "1",
  "workspaceId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seqera/latest/actions/list-workspace-participants?${params}`, {
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
| `max` | number | no |  |
| `offset` | number | no |  |
| `orgId` | number | yes |  |
| `search` | string | no |  |
| `workspaceId` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "participants": [
        {
          "email": "ava@example.com",
          "firstName": "Ava",
          "lastName": "Chen",
          "memberId": 1,
          "orgRole": "string",
          "participantId": 1,
          "teamAvatarUrl": "https://example.com",
          "teamId": 1,
          "teamName": "Ava Chen",
          "type": "string",
          "userAvatarUrl": "https://example.com",
          "userName": "Ava Chen",
          "wspRole": "string"
        }
      ],
      "totalSize": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `participants` | array<object> | Workspace participants. |
| `participants[].email` | string | Participant email address. |
| `participants[].firstName` | string | Participant first name. |
| `participants[].lastName` | string | Participant last name. |
| `participants[].memberId` | number | Organization member ID. |
| `participants[].orgRole` | string | Organization role. |
| `participants[].participantId` | number | Workspace participant ID. |
| `participants[].teamAvatarUrl` | string | Team avatar URL. |
| `participants[].teamId` | number | Team ID. |
| `participants[].teamName` | string | Team name. |
| `participants[].type` | string | Participant type. |
| `participants[].userAvatarUrl` | string | User avatar URL. |
| `participants[].userName` | string | Participant username. |
| `participants[].wspRole` | string | Workspace role. |
| `totalSize` | number | Total number of participants returned. |

## Native endpoint

Through the native Seqera API, this operation is `GET /orgs/:orgId/workspaces/:workspaceId/participants` (base URL `https://api.cloud.seqera.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-workspace-participants.md) for the provider-specific parameters and requirements.

