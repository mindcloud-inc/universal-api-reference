# Create site with Appwrite

Creates a new site in your Appwrite project.

## Endpoint

- **Method:** `POST`
- **Path:** `/sites`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Create site](https://appwrite.io/docs/references/cloud/server-rest/sites)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `siteId` | body | `string` | yes | Site ID. Choose a custom ID or generate a random ID with `ID.unique()`. Valid chars are a-z, A-Z, 0-9, period, hyphen, and underscore. Can't start with a special char. Max length is 36 chars. |
| `name` | body | `string` | yes | Site name. Max length: 128 chars. |
| `framework` | body | `string` | yes | Sites framework. |
| `enabled` | body | `boolean` | no | Is site enabled? When set to 'disabled', users cannot access the site but Server SDKs with and API key can still access the site. No data is lost when this is toggled. |
| `logging` | body | `boolean` | no | When disabled, request logs will exclude logs and errors, and site responses will be slightly faster. |
| `timeout` | body | `number` | no | Maximum request time in seconds. |
| `installCommand` | body | `string` | no | Install Command. |
| `buildCommand` | body | `string` | no | Build Command. |
| `outputDirectory` | body | `string` | no | Output Directory for site. |
| `buildRuntime` | body | `string` | yes | Runtime to use during build step. |
| `adapter` | body | `string` | no | Framework adapter defining rendering strategy. Allowed values are: static, ssr |
| `installationId` | body | `string` | no | Appwrite Installation ID for VCS (Version Control System) deployment. |
| `fallbackFile` | body | `string` | no | Fallback file for single page application sites. |
| `providerRepositoryId` | body | `string` | no | Repository ID of the repo linked to the site. |
| `providerBranch` | body | `string` | no | Production branch for the repo linked to the site. |
| `providerSilentMode` | body | `boolean` | no | Is the VCS (Version Control System) connection in silent mode for the repo linked to the site? In silent mode, comments will not be made on commits and pull requests. |
| `providerRootDirectory` | body | `string` | no | Path to site code in the linked repo. |
| `specification` | body | `string` | no | Framework specification for the site and builds. |
