# Appwrite: Update function

Updates the function in your Appwrite project.

```
PUT https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/functions-update
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Appwrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/functions-update" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "functionId": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/functions-update', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "functionId": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `events` | string | no | Events list. Maximum of 100 events are allowed. |
| `execute` | string | no | An array of role strings with execution permissions. By default no user is granted with any execute permissions. [learn more about roles](https://appwrite.io/docs/permissions#permission-roles). Maximum of 100 roles are allowed, each 64 characters long. |
| `functionId` | string | yes | Function ID. |
| `scopes` | string | no | List of scopes allowed for API Key auto-generated for every execution. Maximum of 100 scopes are allowed. |
| `name` | string | yes | Function name. Max length: 128 chars. |
| `runtime` | string | no | Execution runtime. |
| `execute[]` | array<string> | no | An array of role strings with execution permissions. By default no user is granted with any execute permissions. [learn more about roles](https://appwrite.io/docs/permissions#permission-roles). Maximum of 100 roles are allowed, each 64 characters long. |
| `events[]` | array<string> | no | Events list. Maximum of 100 events are allowed. |
| `schedule` | string | no | Schedule CRON syntax. |
| `timeout` | number | no | Maximum execution time in seconds. |
| `enabled` | boolean | no | Is function enabled? When set to 'disabled', users cannot access the function but Server SDKs with and API key can still access the function. No data is lost when this is toggled. |
| `logging` | boolean | no | When disabled, executions will exclude logs and errors, and will be slightly faster. |
| `entrypoint` | string | no | Entrypoint File. This path is relative to the "providerRootDirectory". |
| `commands` | string | no | Build Commands. |
| `scopes[]` | array<string> | no | List of scopes allowed for API Key auto-generated for every execution. Maximum of 100 scopes are allowed. |
| `installationId` | string | no | Appwrite Installation ID for VCS (Version Controle System) deployment. |
| `providerRepositoryId` | string | no | Repository ID of the repo linked to the function |
| `providerBranch` | string | no | Production branch for the repo linked to the function |
| `providerSilentMode` | boolean | no | Is the VCS (Version Control System) connection in silent mode for the repo linked to the function? In silent mode, comments will not be made on commits and pull requests. |
| `providerRootDirectory` | string | no | Path to function code in the linked repo. |
| `specification` | string | no | Runtime specification for the function and builds. |

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

Through the native Appwrite API, this operation is `PUT /functions/{functionId}` (base URL `https://cloud.appwrite.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/functions-update.md) for the provider-specific parameters and requirements.

