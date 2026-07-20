# List Sources In Source Group with Better Stack Telemetry

Retrieves sources in a source group from Better Stack Telemetry.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/source-groups/:id/sources`
- **Base URL:** `https://telemetry.betterstack.com`
- **Official documentation:** [List Sources In Source Group](https://betterstack.com/docs/logs/api/listing-sources-in-source-group/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | ID of the source group whose sources to list |
