# Get Trace with Langfuse

Retrieves a trace from Langfuse.

## Endpoint

- **Method:** `GET`
- **Path:** `/traces/:traceId`
- **Base URL:** `https://cloud.langfuse.com/api/public`
- **Official documentation:** [Get Trace](https://api.reference.langfuse.com/#tag/Trace/GET/api/public/traces/{traceId})

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `fields` | query | `string` | no |
| `traceId` | path | `string` | yes |
