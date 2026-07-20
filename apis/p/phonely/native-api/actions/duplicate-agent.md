# Duplicate Agent with Phonely

Creates a duplicate agent in Phonely.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/duplicate-agent`
- **Base URL:** `https://app.phonely.ai`
- **Official documentation:** [Duplicate Agent](https://docs.phonely.ai/api-reference/endpoint/duplicate-agent)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uid` | body | `string` | yes | Your Phonely user ID. |
| `agentId` | body | `string` | yes | The ID of the agent to duplicate. |
