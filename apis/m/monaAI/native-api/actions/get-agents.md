# Get Agents with Mona AI

Retrieves agents from Mona AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/database/getAgentsFromDatabase`
- **Base URL:** `https://api.mona-ai.cloud`
- **Official documentation:** [Get Agents](https://api-docs.mona-ai.cloud/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `category` | body | `string` | no | Filter agents by category. |
| `isActive` | body | `boolean` | no | Filter agents by active state. |
| `typeOfAgent` | body | `string` | no | Filter agents by type, such as multi. |
