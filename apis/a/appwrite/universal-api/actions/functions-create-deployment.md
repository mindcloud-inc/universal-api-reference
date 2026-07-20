# Appwrite: Create deployment

Creates a new deployment in your Appwrite project.

```
POST https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/functions-create-deployment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Appwrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/functions-create-deployment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "functionId": "string",
  "code": "string",
  "activate": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/functions-create-deployment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "functionId": "string",
    "code": "string",
    "activate": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `functionId` | string | yes | Function ID. |
| `entrypoint` | string | no | Entrypoint File. |
| `commands` | string | no | Build Commands. |
| `code` | file | yes | Gzip file with your code package. When used with the Appwrite CLI, pass the path to your code directory, and the CLI will automatically package your code. Use a path that is within the current directory. |
| `activate` | boolean | yes | Automatically activate the deployment when it is finished building. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "$createdAt": "string",
      "$id": "string",
      "$updatedAt": "string",
      "activate": true,
      "buildDuration": 1,
      "buildId": "string",
      "buildLogs": "string",
      "buildSize": 1,
      "entrypoint": "string",
      "providerBranch": "string",
      "providerBranchUrl": "https://example.com",
      "providerCommitAuthor": "string",
      "providerCommitAuthorUrl": "https://example.com",
      "providerCommitHash": "string",
      "providerCommitMessage": "string",
      "providerCommitUrl": "https://example.com",
      "providerRepositoryName": "Ava Chen",
      "providerRepositoryOwner": "string",
      "providerRepositoryUrl": "https://example.com",
      "resourceId": "string",
      "resourceType": "string",
      "screenshotDark": "string",
      "screenshotLight": "string",
      "sourceSize": 1,
      "status": "string",
      "totalSize": 1,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `$createdAt` | string |  |
| `$id` | string |  |
| `$updatedAt` | string |  |
| `activate` | boolean |  |
| `buildDuration` | number |  |
| `buildId` | string |  |
| `buildLogs` | string |  |
| `buildSize` | number |  |
| `entrypoint` | string |  |
| `providerBranch` | string |  |
| `providerBranchUrl` | string |  |
| `providerCommitAuthor` | string |  |
| `providerCommitAuthorUrl` | string |  |
| `providerCommitHash` | string |  |
| `providerCommitMessage` | string |  |
| `providerCommitUrl` | string |  |
| `providerRepositoryName` | string |  |
| `providerRepositoryOwner` | string |  |
| `providerRepositoryUrl` | string |  |
| `resourceId` | string |  |
| `resourceType` | string |  |
| `screenshotDark` | string |  |
| `screenshotLight` | string |  |
| `sourceSize` | number |  |
| `status` | string |  |
| `totalSize` | number |  |
| `type` | string |  |

## Native endpoint

Through the native Appwrite API, this operation is `POST /functions/{functionId}/deployments` (base URL `https://cloud.appwrite.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/functions-create-deployment.md) for the provider-specific parameters and requirements.

