# Xata: Update branch details



```
PUT https://connect.mindcloud.co/v1/universal/xata/latest/actions/update-branch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Xata `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/xata/latest/actions/update-branch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "organizationID": "string",
  "projectID": "string",
  "branchID": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/xata/latest/actions/update-branch', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "organizationID": "string",
    "projectID": "string",
    "branchID": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `organizationID` | string | yes | Unique identifier of the organization containing the project |
| `projectID` | string | yes | Unique identifier of the project containing the branch |
| `branchID` | string | yes | Unique identifier of the branch to update |
| `name` | string | no | New name for the branch |
| `description` | string | no | New description for the branch (max 50 characters) |
| `replicas` | number | no | Number of database replicas to scale to |
| `storage` | number | no | Branch storage in GiB (gigabytes) |
| `instanceType` | string | no | New instance type for the branch |
| `backupConfiguration` | object | no |  |
| `hibernate` | boolean | no | Enabled when the branch should be hibernated, disabled if it needs to be reactivated. |
| `scaleToZero` | object | no |  |
| `postgresConfigurationParameters` | object | no | Arbitrary PostgreSQL configuration parameters for the cluster |
| `preloadLibraries[]` | array | no | List of PostgreSQL extensions and libraries to preload |
| `image` | string | no | PostgreSQL image to use for the database instances |

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

Through the native Xata API, this operation is `PATCH /organizations/:organizationID/projects/:projectID/branches/:branchID` (base URL `https://api.xata.tech`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-branch.md) for the provider-specific parameters and requirements.

