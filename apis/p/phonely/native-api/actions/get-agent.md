# Get Agent with Phonely

Retrieves an agent from Phonely.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/get-agent`
- **Base URL:** `https://app.phonely.ai`
- **Official documentation:** [Get Agent](https://docs.phonely.ai/api-reference/endpoint/get-agent)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uid` | body | `string` | yes | The Phonely user ID that owns the target agent. |
| `agentId` | body | `string` | yes | The Phonely agent ID to retrieve. |
