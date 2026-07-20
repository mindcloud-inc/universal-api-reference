# List functions with Appwrite

Retrieves a list of functions from your Appwrite project.

## Endpoint

- **Method:** `GET`
- **Path:** `/functions`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [List functions](https://appwrite.io/docs/references/cloud/server-rest/functions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `queries[]` | query | `array<string>` | no | Array of query strings generated using the Query class provided by the SDK. [Learn more about queries](https://appwrite.io/docs/queries). Maximum of 100 queries are allowed, each 4096 characters long. You may filter on the following attributes: name, enabled, runtime, deploymentId, schedule, scheduleNext, schedulePrevious, timeout, entrypoint, commands, installationId Send multiple values as a array. |
| `search` | query | `string` | no | Search term to filter your list results. Max length: 256 chars. |
| `total` | query | `boolean` | no | When set to false, the total count returned will be 0 and will not be calculated. |
