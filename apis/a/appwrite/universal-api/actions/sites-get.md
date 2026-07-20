# Appwrite: Get site

Retrieves site details from your Appwrite project.

```
GET https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/sites-get
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Appwrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/sites-get?connectionId=$CONNECTION_ID&siteId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "siteId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/sites-get?${params}`, {
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
| `siteId` | string | yes | Site ID. |

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

Through the native Appwrite API, this operation is `GET /sites/{siteId}` (base URL `https://cloud.appwrite.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/sites-get.md) for the provider-specific parameters and requirements.

