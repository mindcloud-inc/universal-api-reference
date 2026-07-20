# List users with Appwrite

Retrieves a list of users from your Appwrite project.

## Endpoint

- **Method:** `GET`
- **Path:** `/users`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [List users](https://appwrite.io/docs/references/cloud/server-rest/users)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `queries[]` | query | `array<string>` | no | Array of query strings generated using the Query class provided by the SDK. [Learn more about queries](https://appwrite.io/docs/queries). Maximum of 100 queries are allowed, each 4096 characters long. You may filter on the following attributes: name, email, phone, status, passwordUpdate, registration, emailVerification, phoneVerification, labels Send multiple values as a array. |
| `search` | query | `string` | no | Search term to filter your list results. Max length: 256 chars. |
| `total` | query | `boolean` | no | When set to false, the total count returned will be 0 and will not be calculated. |
