# Remove URL Group Endpoints with QStash

Removes endpoints from a QStash URL Group.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v2/topics/:urlGroupName/endpoints`
- **Base URL:** `https://qstash-eu-central-1.upstash.io`
- **Official documentation:** [Remove URL Group Endpoints](https://upstash.com/docs/qstash/sdks/ts/examples/url-groups)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `urlGroupName` | path | `string` | yes | Name of the URL Group. |
| `endpoints[]` | body | `array<object>` | yes | Endpoints to remove from the URL Group. |
