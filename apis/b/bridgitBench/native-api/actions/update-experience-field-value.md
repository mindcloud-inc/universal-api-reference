# Update Experience Field Value with Bridgit Bench

## Endpoint

- **Method:** `POST`
- **Path:** `/rp/api/v1/accounts/:accountId/experience-fields/:experienceFieldId/values/:experienceFieldValueId`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Update Experience Field Value](https://developers.gobridgit.com/reference/experiencefieldvalues_update)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The Account ID |
| `experienceFieldId` | path | `string` | yes | The Experience Field UUID |
| `experienceFieldValueId` | path | `string` | yes | The Experience Field Value ID UUID |
| `name` | body | `string` | yes | Maximum length: 250. |
