# List user targets with Appwrite

Retrieves a list of user targets from your Appwrite project.

## Endpoint

- **Method:** `GET`
- **Path:** `/users/{userId}/targets`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [List user targets](https://appwrite.io/docs/references/cloud/server-rest/users)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `string` | yes | User ID. |
| `queries[]` | query | `array<string>` | no | Array of query strings generated using the Query class provided by the SDK. [Learn more about queries](https://appwrite.io/docs/queries). Maximum of 100 queries are allowed, each 4096 characters long. You may filter on the following attributes: userId, providerId, identifier, providerType Send multiple values as a array. |
| `total` | query | `boolean` | no | When set to false, the total count returned will be 0 and will not be calculated. |
