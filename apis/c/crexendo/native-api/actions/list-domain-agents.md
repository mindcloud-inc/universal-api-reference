# List Domain Agents with Crexendo

Retrieves agents for a domain in Crexendo.

## Endpoint

- **Method:** `GET`
- **Path:** `/domains/:domain/agents`
- **Base URL:** `https://ns-api.com/ns-api/v2`
- **Official documentation:** [List Domain Agents](https://docs.ns-api.com/reference/readagentsdomain)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | path | `string` | yes | Domain identifier, for example apps.mindcloud.co. |
