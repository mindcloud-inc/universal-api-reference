# Xata: Create a new branch from a backup of another branch



```
POST https://connect.mindcloud.co/v1/universal/xata/latest/actions/restore-from-backup
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Xata `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/xata/latest/actions/restore-from-backup" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "organizationID": "string",
  "projectID": "string",
  "branchID": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/xata/latest/actions/restore-from-backup', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "organizationID": "string",
    "projectID": "string",
    "branchID": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `organizationID` | string | yes | Unique identifier of the organization containing the project |
| `projectID` | string | yes | Unique identifier of the project containing the source branch |
| `branchID` | string | yes | Unique identifier of the source branch of the backup |
| `name` | string | yes | Human-readable name of the branch |
| `description` | string | no | Optional description of the branch purpose or contents |
| `scaleToZero` | object | no |  |
| `backupConfiguration` | object | no |  |
| `configuration` | object | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "connectionString": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": "string",
      "name": "Ava Chen",
      "parentID": "string",
      "publicAccess": true,
      "region": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `connectionString` | string | Database connection string for accessing this branch |
| `createdAt` | date | Timestamp when the branch was created |
| `description` | string | Optional description of the branch purpose or contents |
| `id` | string | Unique identifier for the branch |
| `name` | string | Human-readable name of the branch |
| `parentID` | string | Identifier of the parent branch if this is a derived branch, null otherwise |
| `publicAccess` | boolean | Whether the branch allows public access without authentication |
| `region` | string | Geographic region where the branch is deployed |
| `updatedAt` | date | Timestamp when the branch was last updated |

## Native endpoint

Through the native Xata API, this operation is `POST /organizations/:organizationID/projects/:projectID/branches/:branchID/restore` (base URL `https://api.xata.tech`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/restore-from-backup.md) for the provider-specific parameters and requirements.

