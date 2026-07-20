# Get agent with Zillow MLS Data

Retrieves a specific agent from Zillow MLS Data.

## Endpoint

- **Method:** `GET`
- **Path:** `/:dataset/agents/:agentId`
- **Base URL:** `https://api.bridgedataoutput.com/api/v2`
- **Official documentation:** [Get agent](https://www.zillowgroup.com/developers/api/mls-broker-data/mls-listings/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dataset` | path | `string` | yes | Bridge dataset code that contains the agent. |
| `agentId` | path | `string` | yes | Agent identifier from the Bridge dataset. |
