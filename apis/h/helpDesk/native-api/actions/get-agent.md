# Get Agent with HelpDesk

Retrieves an agent from HelpDesk.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/agents/:agentID`
- **Base URL:** `https://api.helpdesk.com`
- **Official documentation:** [Get Agent](https://api.helpdesk.com/docs#tag/Agents/operation/agentsRead)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agentID` | path | `string` | yes | Unique HelpDesk agent ID. |
