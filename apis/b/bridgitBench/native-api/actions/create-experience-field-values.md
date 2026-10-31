# Create Experience Field Values with Bridgit Bench

## Endpoint

- **Method:** `POST`
- **Path:** `/rp/api/v1/accounts/:accountId/experience-fields/:experienceFieldId/values`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Create Experience Field Values](https://developers.gobridgit.com/reference/experiencefieldvalues_create)

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
| `payload[]` | body | `array<object>` | no | — |
| `payload[].name` | body | `string` | yes | Maximum length: 250. |
