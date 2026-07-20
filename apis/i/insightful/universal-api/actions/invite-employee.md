# Insightful: Invite Employee

Invites a new employee to your Insightful account.

```
POST https://connect.mindcloud.co/v1/universal/insightful/latest/actions/invite-employee
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Insightful `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/insightful/latest/actions/invite-employee" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "name": "Ava Chen",
  "sharedSettingsId": "string",
  "teamId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/insightful/latest/actions/invite-employee', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "name": "Ava Chen",
    "sharedSettingsId": "string",
    "teamId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | The employee email address. |
| `name` | string | yes | The employee name. |
| `sharedSettingsId` | string | yes | The shared settings ID to apply to the employee. |
| `teamId` | string | yes | The team ID the employee belongs to. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "deactivated": 1,
      "email": "ava@example.com",
      "id": "string",
      "identifier": "string",
      "invited": 1,
      "localDataRetention": 1,
      "logLevel": "string",
      "modelName": "Ava Chen",
      "name": "Ava Chen",
      "organizationId": "string",
      "pseudonymId": 1,
      "sharedSettingsId": "string",
      "teamId": "string",
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string |  |
| `createdAt` | date |  |
| `deactivated` | number |  |
| `email` | string |  |
| `id` | string |  |
| `identifier` | string |  |
| `invited` | number |  |
| `localDataRetention` | number |  |
| `logLevel` | string |  |
| `modelName` | string |  |
| `name` | string |  |
| `organizationId` | string |  |
| `pseudonymId` | number |  |
| `sharedSettingsId` | string |  |
| `teamId` | string |  |
| `type` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Insightful API, this operation is `POST /employee` (base URL `https://app.insightful.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/invite-employee.md) for the provider-specific parameters and requirements.

