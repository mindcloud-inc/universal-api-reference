# List Threads with Cirra

Retrieves Cirra threads for the authenticated user.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/cirra/threads`
- **Base URL:** `http://api-public:9801`

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `archived` | query | `boolean` | no | When true, list archived threads instead of active threads. |
