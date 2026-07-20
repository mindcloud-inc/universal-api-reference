# Get Execution Results with Shuffler

Retrieves execution results from Shuffler.

## Endpoint

- **Method:** `POST`
- **Path:** `/streams/results`
- **Base URL:** `https://shuffler.io/api/v1`
- **Official documentation:** [Get Execution Results](https://shuffler.io/docs/API#get-execution-results)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `authorization` | body | `string` | yes | Execution authorization token. |
| `execution_id` | body | `string` | yes | Execution identifier. |
