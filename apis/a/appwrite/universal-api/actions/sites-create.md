# Appwrite: Create site

Creates a new site in your Appwrite project.

```
POST https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/sites-create
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Appwrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/sites-create" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "siteId": "string",
  "name": "Ava Chen",
  "framework": "string",
  "buildRuntime": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/sites-create', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "siteId": "string",
    "name": "Ava Chen",
    "framework": "string",
    "buildRuntime": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `siteId` | string | yes | Site ID. Choose a custom ID or generate a random ID with `ID.unique()`. Valid chars are a-z, A-Z, 0-9, period, hyphen, and underscore. Can't start with a special char. Max length is 36 chars. |
| `name` | string | yes | Site name. Max length: 128 chars. |
| `framework` | string | yes | Sites framework. |
| `enabled` | boolean | no | Is site enabled? When set to 'disabled', users cannot access the site but Server SDKs with and API key can still access the site. No data is lost when this is toggled. |
| `logging` | boolean | no | When disabled, request logs will exclude logs and errors, and site responses will be slightly faster. |
| `timeout` | number | no | Maximum request time in seconds. |
| `installCommand` | string | no | Install Command. |
| `buildCommand` | string | no | Build Command. |
| `outputDirectory` | string | no | Output Directory for site. |
| `buildRuntime` | string | yes | Runtime to use during build step. |
| `adapter` | string | no | Framework adapter defining rendering strategy. Allowed values are: static, ssr |
| `installationId` | string | no | Appwrite Installation ID for VCS (Version Control System) deployment. |
| `fallbackFile` | string | no | Fallback file for single page application sites. |
| `providerRepositoryId` | string | no | Repository ID of the repo linked to the site. |
| `providerBranch` | string | no | Production branch for the repo linked to the site. |
| `providerSilentMode` | boolean | no | Is the VCS (Version Control System) connection in silent mode for the repo linked to the site? In silent mode, comments will not be made on commits and pull requests. |
| `providerRootDirectory` | string | no | Path to site code in the linked repo. |
| `specification` | string | no | Framework specification for the site and builds. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "$createdAt": "string",
      "$id": "string",
      "$updatedAt": "string",
      "adapter": "string",
      "buildCommand": "string",
      "buildRuntime": "string",
      "deploymentCreatedAt": "string",
      "deploymentId": "string",
      "deploymentScreenshotDark": "string",
      "deploymentScreenshotLight": "string",
      "enabled": true,
      "fallbackFile": "string",
      "framework": "string",
      "installationId": "string",
      "installCommand": "string",
      "latestDeploymentCreatedAt": "string",
      "latestDeploymentId": "string",
      "latestDeploymentStatus": "string",
      "live": true,
      "logging": true,
      "name": "Ava Chen",
      "outputDirectory": "string",
      "providerBranch": "string",
      "providerRepositoryId": "string",
      "providerRootDirectory": "string",
      "providerSilentMode": true,
      "specification": "string",
      "timeout": 1,
      "vars": [
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
| `$createdAt` | string | Site creation date in ISO 8601 format. |
| `$id` | string | Site ID. |
| `$updatedAt` | string | Site update date in ISO 8601 format. |
| `adapter` | string | Site framework adapter. |
| `buildCommand` | string | The build command used to build the site. |
| `buildRuntime` | string | Site build runtime. |
| `deploymentCreatedAt` | string | Active deployment creation date in ISO 8601 format. |
| `deploymentId` | string | Site's active deployment ID. |
| `deploymentScreenshotDark` | string | Screenshot of active deployment with dark theme preference file ID. |
| `deploymentScreenshotLight` | string | Screenshot of active deployment with light theme preference file ID. |
| `enabled` | boolean | Site enabled. |
| `fallbackFile` | string | Name of fallback file to use instead of 404 page. If null, Appwrite 404 page will be displayed. |
| `framework` | string | Site framework. |
| `installationId` | string | Site VCS (Version Control System) installation id. |
| `installCommand` | string | The install command used to install the site dependencies. |
| `latestDeploymentCreatedAt` | string | Latest deployment creation date in ISO 8601 format. |
| `latestDeploymentId` | string | Site's latest deployment ID. |
| `latestDeploymentStatus` | string | Status of latest deployment. Possible values are "waiting", "processing", "building", "ready", and "failed". |
| `live` | boolean | Is the site deployed with the latest configuration? This is set to false if you've changed an environment variables, entrypoint, commands, or other settings that needs redeploy to be applied. When the value is false, redeploy the site to update it with the latest configuration. |
| `logging` | boolean | When disabled, request logs will exclude logs and errors, and site responses will be slightly faster. |
| `name` | string | Site name. |
| `outputDirectory` | string | The directory where the site build output is located. |
| `providerBranch` | string | VCS (Version Control System) branch name |
| `providerRepositoryId` | string | VCS (Version Control System) Repository ID |
| `providerRootDirectory` | string | Path to site in VCS (Version Control System) repository |
| `providerSilentMode` | boolean | Is VCS (Version Control System) connection is in silent mode? When in silence mode, no comments will be posted on the repository pull or merge requests |
| `specification` | string | Machine specification for builds and executions. |
| `timeout` | number | Site request timeout in seconds. |
| `vars` | array<object> | Site variables. |

## Native endpoint

Through the native Appwrite API, this operation is `POST /sites` (base URL `https://cloud.appwrite.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/sites-create.md) for the provider-specific parameters and requirements.

