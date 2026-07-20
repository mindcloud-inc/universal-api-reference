# List Domain SMS Numbers with Crexendo

Retrieves SMS numbers for a domain in Crexendo.

## Endpoint

- **Method:** `GET`
- **Path:** `/domains/:domain/smsnumbers`
- **Base URL:** `https://ns-api.com/ns-api/v2`
- **Official documentation:** [List Domain SMS Numbers](https://docs.ns-api.com/reference/getsmsnumbersfordomain)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | path | `string` | yes | Domain identifier, for example apps.mindcloud.co. |
