# External Query Stream with Tako

Streams external query results from Tako.

## Endpoint

- **Method:** `POST`
- **Path:** `/external/v1/query`
- **Base URL:** `https://tako.com/api`
- **Official documentation:** [External Query Stream](https://docs.tako.com/api-reference/openapi.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | yes | Query text to send through Tako's external streaming interface. |
| `thread_id` | body | `string` | no | Optional thread ID for follow-up external queries. |
