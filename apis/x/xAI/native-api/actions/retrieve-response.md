# Retrieve Response with xAI

Retrieves a response from the xAI API.

## Endpoint

- **Method:** `GET`
- **Path:** `/responses/:response_id`
- **Base URL:** `https://api.x.ai/v1`
- **Official documentation:** [Retrieve Response](https://docs.x.ai/developers/rest-api-reference/inference/chat#retrieve-response)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `response_id` | path | `string` | no | Response ID returned by Create Response. |
