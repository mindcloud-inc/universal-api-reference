# Xata: Get branch details



```
GET https://connect.mindcloud.co/v1/universal/xata/latest/actions/describe-branch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Xata `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xata/latest/actions/describe-branch?connectionId=$CONNECTION_ID&organizationID=string&projectID=string&branchID=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationID": "string",
  "projectID": "string",
  "branchID": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xata/latest/actions/describe-branch?${params}`, {
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
| `organizationID` | string | yes | Unique identifier of the organization containing the project |
| `projectID` | string | yes | Unique identifier of the project containing the branch |
| `branchID` | string | yes | Unique identifier of the branch to retrieve details for |

## Response

```json
{
  "success": true,
  "data": [
    {
      "backupConfiguration": {},
      "backupsEnabled": true,
      "configuration": {},
      "connectionString": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": "string",
      "name": "Ava Chen",
      "parentID": "string",
      "publicAccess": true,
      "region": "string",
      "scaleToZero": {},
      "status": {},
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `backupConfiguration` | object |  |
| `backupsEnabled` | boolean | Whether the branch is in a region that supports backups |
| `configuration` | object |  |
| `connectionString` | string | Database connection string for accessing this branch |
| `createdAt` | date | Timestamp when the branch was created |
| `description` | string | Optional description of the branch purpose or contents |
| `id` | string | Unique identifier for the branch |
| `name` | string | Human-readable name of the branch |
| `parentID` | string | Identifier of the parent branch if this is a derived branch, null otherwise |
| `publicAccess` | boolean | Whether the branch allows public access without authentication |
| `region` | string | Geographic region where the branch is deployed |
| `scaleToZero` | object |  |
| `status` | object |  |
| `updatedAt` | date | Timestamp when the branch was last updated |

## Native endpoint

Through the native Xata API, this operation is `GET /organizations/:organizationID/projects/:projectID/branches/:branchID` (base URL `https://api.xata.tech`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/describe-branch.md) for the provider-specific parameters and requirements.

