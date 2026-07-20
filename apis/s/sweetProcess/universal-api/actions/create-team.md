# SweetProcess: Create Team



```
POST https://connect.mindcloud.co/v1/universal/sweetProcess/latest/actions/create-team
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SweetProcess `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sweetProcess/latest/actions/create-team" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sweetProcess/latest/actions/create-team', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | The SweetProcess team name. |
| `description` | string | no | Optional team description. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountWide": true,
      "contentType": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "htmlUrl": "https://example.com",
      "id": 1,
      "modifiedAt": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "numberOfPolicies": 1,
      "numberOfProcedures": 1,
      "numberOfProcesses": 1,
      "numManagers": 1,
      "numReaders": 1,
      "numTeammates": 1,
      "slug": "string",
      "teammatesCanAssignTask": true,
      "url": "https://example.com",
      "users": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountWide` | boolean | Whether the team is account-wide. |
| `contentType` | string | The SweetProcess content type for the record, for example team. |
| `createdAt` | date | When the team was created. |
| `description` | string | The team description. |
| `htmlUrl` | string | The SweetProcess web URL for the team. |
| `id` | number | The numeric SweetProcess team ID. |
| `modifiedAt` | date | When the team was last modified. |
| `name` | string | The team name. |
| `numberOfPolicies` | number | The number of policies in the team. |
| `numberOfProcedures` | number | The number of procedures in the team. |
| `numberOfProcesses` | number | The number of processes in the team. |
| `numManagers` | number | The number of managers in the team. |
| `numReaders` | number | The number of readers in the team. |
| `numTeammates` | number | The number of teammates in the team. |
| `slug` | string | The team slug. |
| `teammatesCanAssignTask` | boolean | Whether teammates can assign tasks in the team. |
| `url` | string | The API URL for the SweetProcess team. |
| `users` | array<object> | The users currently associated with the team. |

## Native endpoint

Through the native SweetProcess API, this operation is `POST /teams/` (base URL `https://www.sweetprocess.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-team.md) for the provider-specific parameters and requirements.

