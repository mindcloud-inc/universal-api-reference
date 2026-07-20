# Add URL Group Endpoints with QStash

Adds endpoints to a QStash URL Group, creating it if needed.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/topics/:urlGroupName/endpoints`
- **Base URL:** `https://qstash-eu-central-1.upstash.io`
- **Official documentation:** [Add URL Group Endpoints](https://upstash.com/docs/qstash/howto/url-group-endpoint)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `urlGroupName` | path | `string` | yes | Name of the URL Group. |
| `endpoints[]` | body | `array<object>` | yes | Endpoints to add to the URL Group. |
