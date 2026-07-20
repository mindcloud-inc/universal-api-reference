# List provider logs with Appwrite

Retrieves a list of provider logs from your Appwrite project.

## Endpoint

- **Method:** `GET`
- **Path:** `/messaging/providers/{providerId}/logs`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [List provider logs](https://appwrite.io/docs/references/cloud/server-rest/messaging)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `providerId` | path | `string` | yes | Provider ID. |
| `queries[]` | query | `array<string>` | no | Array of query strings generated using the Query class provided by the SDK. [Learn more about queries](https://appwrite.io/docs/queries). Only supported methods are limit and offset Send multiple values as a array. |
| `total` | query | `boolean` | no | When set to false, the total count returned will be 0 and will not be calculated. |
