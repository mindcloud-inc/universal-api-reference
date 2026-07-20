# Get Design Pages with Canva

Retrieves pages for a Canva design.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/designs/:designId/pages`
- **Base URL:** `https://api.canva.com/rest`
- **Official documentation:** [Get Design Pages](https://www.canva.dev/docs/connect/api-reference/designs/get-design-pages/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `designId` | path | `string` | yes | The Canva design ID. |
