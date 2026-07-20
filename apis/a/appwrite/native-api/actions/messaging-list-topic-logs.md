# List topic logs with Appwrite

Retrieves a list of topic logs from your Appwrite project.

## Endpoint

- **Method:** `GET`
- **Path:** `/messaging/topics/{topicId}/logs`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [List topic logs](https://appwrite.io/docs/references/cloud/server-rest/messaging)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `topicId` | path | `string` | yes | Topic ID. |
| `queries[]` | query | `array<string>` | no | Array of query strings generated using the Query class provided by the SDK. [Learn more about queries](https://appwrite.io/docs/queries). Only supported methods are limit and offset Send multiple values as a array. |
| `total` | query | `boolean` | no | When set to false, the total count returned will be 0 and will not be calculated. |
