# Update site with Appwrite

Updates the site in your Appwrite project.

## Endpoint

- **Method:** `PUT`
- **Path:** `/sites/{siteId}`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Update site](https://appwrite.io/docs/references/cloud/server-rest/sites)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `siteId` | path | `string` | yes | Site ID. |
| `name` | body | `string` | yes | Site name. Max length: 128 chars. |
| `framework` | body | `string` | yes | Sites framework. |
| `enabled` | body | `boolean` | no | Is site enabled? When set to 'disabled', users cannot access the site but Server SDKs with and API key can still access the site. No data is lost when this is toggled. |
| `logging` | body | `boolean` | no | When disabled, request logs will exclude logs and errors, and site responses will be slightly faster. |
| `timeout` | body | `number` | no | Maximum request time in seconds. |
| `installCommand` | body | `string` | no | Install Command. |
| `buildCommand` | body | `string` | no | Build Command. |
| `outputDirectory` | body | `string` | no | Output Directory for site. |
| `buildRuntime` | body | `string` | no | Runtime to use during build step. |
| `adapter` | body | `string` | no | Framework adapter defining rendering strategy. Allowed values are: static, ssr |
| `fallbackFile` | body | `string` | no | Fallback file for single page application sites. |
| `installationId` | body | `string` | no | Appwrite Installation ID for VCS (Version Control System) deployment. |
| `providerRepositoryId` | body | `string` | no | Repository ID of the repo linked to the site. |
| `providerBranch` | body | `string` | no | Production branch for the repo linked to the site. |
| `providerSilentMode` | body | `boolean` | no | Is the VCS (Version Control System) connection in silent mode for the repo linked to the site? In silent mode, comments will not be made on commits and pull requests. |
| `providerRootDirectory` | body | `string` | no | Path to site code in the linked repo. |
| `specification` | body | `string` | no | Framework specification for the site and builds. |
