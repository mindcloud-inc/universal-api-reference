# List Campaigns with CueGrowth

## Endpoint

- **Method:** `GET`
- **Path:** `/campaigns`
- **Base URL:** `https://api.cuegrowth.ai/public/api`
- **Official documentation:** [List Campaigns](https://cuegrowth.ai/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | query | `string` | no | Filter campaigns by name. |
| `type` | query | `string` | no | Filter campaigns by type. |
| `action_support` | query | `boolean` | no | Return only campaigns that can be used in CueGrowth action APIs. |
