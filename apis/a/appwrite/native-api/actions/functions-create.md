# Create function with Appwrite

Creates a new function in your Appwrite project.

## Endpoint

- **Method:** `POST`
- **Path:** `/functions`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Create function](https://appwrite.io/docs/references/cloud/server-rest/functions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `events` | body | `string` | no | Events list. Maximum of 100 events are allowed. |
| `execute` | body | `string` | no | An array of role strings with execution permissions. By default no user is granted with any execute permissions. [learn more about roles](https://appwrite.io/docs/permissions#permission-roles). Maximum of 100 roles are allowed, each 64 characters long. |
| `functionId` | body | `string` | yes | Function ID. Choose a custom ID or generate a random ID with `ID.unique()`. Valid chars are a-z, A-Z, 0-9, period, hyphen, and underscore. Can't start with a special char. Max length is 36 chars. |
| `scopes` | body | `string` | no | List of scopes allowed for API key auto-generated for every execution. Maximum of 100 scopes are allowed. |
| `name` | body | `string` | yes | Function name. Max length: 128 chars. |
| `runtime` | body | `string` | yes | Execution runtime. |
| `execute[]` | body | `array<string>` | no | An array of role strings with execution permissions. By default no user is granted with any execute permissions. [learn more about roles](https://appwrite.io/docs/permissions#permission-roles). Maximum of 100 roles are allowed, each 64 characters long. |
| `events[]` | body | `array<string>` | no | Events list. Maximum of 100 events are allowed. |
| `schedule` | body | `string` | no | Schedule CRON syntax. |
| `timeout` | body | `number` | no | Function maximum execution time in seconds. |
| `enabled` | body | `boolean` | no | Is function enabled? When set to 'disabled', users cannot access the function but Server SDKs with and API key can still access the function. No data is lost when this is toggled. |
| `logging` | body | `boolean` | no | When disabled, executions will exclude logs and errors, and will be slightly faster. |
| `entrypoint` | body | `string` | no | Entrypoint File. This path is relative to the "providerRootDirectory". |
| `commands` | body | `string` | no | Build Commands. |
| `scopes[]` | body | `array<string>` | no | List of scopes allowed for API key auto-generated for every execution. Maximum of 100 scopes are allowed. |
| `installationId` | body | `string` | no | Appwrite Installation ID for VCS (Version Control System) deployment. |
| `providerRepositoryId` | body | `string` | no | Repository ID of the repo linked to the function. |
| `providerBranch` | body | `string` | no | Production branch for the repo linked to the function. |
| `providerSilentMode` | body | `boolean` | no | Is the VCS (Version Control System) connection in silent mode for the repo linked to the function? In silent mode, comments will not be made on commits and pull requests. |
| `providerRootDirectory` | body | `string` | no | Path to function code in the linked repo. |
| `specification` | body | `string` | no | Runtime specification for the function and builds. |
