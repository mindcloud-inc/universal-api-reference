# Appwrite: Get function

Retrieves function details from your Appwrite project.

```
GET https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/functions-get
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Appwrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/functions-get?connectionId=$CONNECTION_ID&functionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "functionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/functions-get?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "$createdAt": "string",
      "$id": "string",
      "$updatedAt": "string",
      "commands": "string",
      "deploymentCreatedAt": "string",
      "deploymentId": "string",
      "enabled": true,
      "entrypoint": "string",
      "events": [
        "string"
      ],
      "execute": [
        "string"
      ],
      "installationId": "string",
      "latestDeploymentCreatedAt": "string",
      "latestDeploymentId": "string",
      "latestDeploymentStatus": "string",
      "live": true,
      "logging": true,
      "name": "Ava Chen",
      "providerBranch": "string",
      "providerRepositoryId": "string",
      "providerRootDirectory": "string",
      "providerSilentMode": true,
      "runtime": "string",
      "schedule": "string",
      "scopes": [
        "string"
      ],
      "specification": "string",
      "timeout": 1,
      "vars": [
        {}
      ],
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `$createdAt` | string | Function creation date in ISO 8601 format. |
| `$id` | string | Function ID. |
| `$updatedAt` | string | Function update date in ISO 8601 format. |
| `commands` | string | The build command used to build the deployment. |
| `deploymentCreatedAt` | string | Active deployment creation date in ISO 8601 format. |
| `deploymentId` | string | Function's active deployment ID. |
| `enabled` | boolean | Function enabled. |
| `entrypoint` | string | The entrypoint file used to execute the deployment. |
| `events` | array<string> | Function trigger events. |
| `execute` | array<string> | Execution permissions. |
| `installationId` | string | Function VCS (Version Control System) installation id. |
| `latestDeploymentCreatedAt` | string | Latest deployment creation date in ISO 8601 format. |
| `latestDeploymentId` | string | Function's latest deployment ID. |
| `latestDeploymentStatus` | string | Status of latest deployment. Possible values are "waiting", "processing", "building", "ready", and "failed". |
| `live` | boolean | Is the function deployed with the latest configuration? This is set to false if you've changed an environment variables, entrypoint, commands, or other settings that needs redeploy to be applied. When the value is false, redeploy the function to update it with the latest configuration. |
| `logging` | boolean | When disabled, executions will exclude logs and errors, and will be slightly faster. |
| `name` | string | Function name. |
| `providerBranch` | string | VCS (Version Control System) branch name |
| `providerRepositoryId` | string | VCS (Version Control System) Repository ID |
| `providerRootDirectory` | string | Path to function in VCS (Version Control System) repository |
| `providerSilentMode` | boolean | Is VCS (Version Control System) connection is in silent mode? When in silence mode, no comments will be posted on the repository pull or merge requests |
| `runtime` | string | Function execution and build runtime. |
| `schedule` | string | Function execution schedule in CRON format. |
| `scopes` | array<string> | Allowed permission scopes. |
| `specification` | string | Machine specification for builds and executions. |
| `timeout` | number | Function execution timeout in seconds. |
| `vars` | array<object> | Function variables. |
| `version` | string | Version of Open Runtimes used for the function. |

## Native endpoint

Through the native Appwrite API, this operation is `GET /functions/{functionId}` (base URL `https://cloud.appwrite.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/functions-get.md) for the provider-specific parameters and requirements.

