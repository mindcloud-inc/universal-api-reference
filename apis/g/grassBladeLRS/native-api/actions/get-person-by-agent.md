# Get Person By Agent with GrassBlade LRS

Retrieves person details from GrassBlade LRS by agent.

## Endpoint

- **Method:** `GET`
- **Path:** `/agents`
- **Base URL:** `https://test.gblrs.com/xAPI`
- **Official documentation:** [Get Person By Agent](https://github.com/adlnet/xAPI-Spec/blob/xAPI-1.0.3/xAPI-Communication.md#agentsres)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agent` | query | `string` | yes | Agent JSON to fetch person information for. |
