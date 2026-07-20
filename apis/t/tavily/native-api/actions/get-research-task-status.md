# Get Research Task Status with Tavily

Retrieves Tavily research task status and results by request ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/research/:request_id`
- **Base URL:** `https://api.tavily.com`
- **Official documentation:** [Get Research Task Status](https://docs.tavily.com/documentation/api-reference/endpoint/research-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `request_id` | path | `string` | yes | The unique identifier of the research task. |
