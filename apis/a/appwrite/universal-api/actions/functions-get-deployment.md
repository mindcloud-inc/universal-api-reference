# Appwrite: Get deployment

Retrieves the deployment from your Appwrite project.

```
GET https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/functions-get-deployment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Appwrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/functions-get-deployment?connectionId=$CONNECTION_ID&functionId=string&deploymentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "functionId": "string",
  "deploymentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/functions-get-deployment?${params}`, {
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
| `functionId` | string | yes | Function ID. |
| `deploymentId` | string | yes | Deployment ID. |

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
| `$createdAt` | string | Deployment creation date in ISO 8601 format. |
| `$id` | string | Deployment ID. |
| `$updatedAt` | string | Deployment update date in ISO 8601 format. |
| `activate` | boolean | Whether the deployment should be automatically activated. |
| `buildDuration` | number | The current build time in seconds. |
| `buildId` | string | The current build ID. |
| `buildLogs` | string | The build logs. |
| `buildSize` | number | The build output size in bytes. |
| `entrypoint` | string | The entrypoint file to use to execute the deployment code. |
| `providerBranch` | string | The branch of the vcs repository |
| `providerBranchUrl` | string | The branch of the vcs repository |
| `providerCommitAuthor` | string | The name of vcs commit author |
| `providerCommitAuthorUrl` | string | The url of vcs commit author |
| `providerCommitHash` | string | The commit hash of the vcs commit |
| `providerCommitMessage` | string | The commit message |
| `providerCommitUrl` | string | The url of the vcs commit |
| `providerRepositoryName` | string | The name of the vcs provider repository |
| `providerRepositoryOwner` | string | The name of the vcs provider repository owner |
| `providerRepositoryUrl` | string | The url of the vcs provider repository |
| `resourceId` | string | Resource ID. |
| `resourceType` | string | Resource type. |
| `screenshotDark` | string | Screenshot with dark theme preference file ID. |
| `screenshotLight` | string | Screenshot with light theme preference file ID. |
| `sourceSize` | number | The code size in bytes. |
| `status` | string | The deployment status. Possible values are "waiting", "processing", "building", "ready", and "failed". |
| `totalSize` | number | The total size in bytes (source and build output). |
| `type` | string | Type of deployment. |

## Native endpoint

Through the native Appwrite API, this operation is `GET /functions/{functionId}/deployments/{deploymentId}` (base URL `https://cloud.appwrite.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/functions-get-deployment.md) for the provider-specific parameters and requirements.

