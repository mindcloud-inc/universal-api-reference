# Get Integration Status with Galileo

Retrieves status for a Galileo integration.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/integrations/:name/status`
- **Base URL:** `https://api.galileo.ai`
- **Official documentation:** [Get Integration Status](https://docs.galileo.ai/api-reference/integrations/get-integration-status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | path | `string` | yes | Integration name from Galileo, for example openai or anthropic. |
