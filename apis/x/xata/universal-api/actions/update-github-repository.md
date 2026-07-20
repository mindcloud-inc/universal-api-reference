# Xata: Update GitHub repository mapping



```
PUT https://connect.mindcloud.co/v1/universal/xata/latest/actions/update-github-repository
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Xata `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/xata/latest/actions/update-github-repository" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "organizationID": "string",
  "projectID": "string",
  "branchID": "string",
  "githubRepositoryID": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/xata/latest/actions/update-github-repository', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "organizationID": "string",
    "projectID": "string",
    "branchID": "string",
    "githubRepositoryID": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `organizationID` | string | yes | Unique identifier of the organization |
| `projectID` | string | yes | Unique identifier of the project |
| `branchID` | string | yes | Unique identifier of the branch |
| `githubRepositoryID` | number | yes | GitHub repository ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "githubRepositoryID": 1,
      "id": "string",
      "project": "string",
      "rootBranchId": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | Timestamp when the mapping was created |
| `githubRepositoryID` | number | GitHub repository ID |
| `id` | string | Unique identifier of the mapping record |
| `project` | string | Project ID this mapping is associated with |
| `rootBranchId` | string | ID of the root Xata branch mapped to this repository |
| `updatedAt` | date | Timestamp when the mapping was last updated |

## Native endpoint

Through the native Xata API, this operation is `PUT /organizations/:organizationID/projects/:projectID/branches/:branchID/githubapp/repository` (base URL `https://api.xata.tech`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-github-repository.md) for the provider-specific parameters and requirements.

