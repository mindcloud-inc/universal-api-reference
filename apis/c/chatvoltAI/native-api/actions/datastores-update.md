# Update Datastore with Chatvolt AI

Updates a datastore in Chatvolt AI.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/datastores/{id}`
- **Base URL:** `https://api.chatvolt.ai`
- **Official documentation:** [Update Datastore](https://docs.chatvolt.ai/api-reference/endpoint/datastores/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | ID of the datastore to be updated. |
| `name` | body | `string` | no | Name for application/json requests. |
| `description` | body | `string` | no | Description for application/json requests. |
| `type` | body | `string` | no | Type for application/json requests. |
| `isPublic` | body | `boolean` | no | IsPublic for application/json requests. |
| `pluginName` | body | `string` | no | PluginName for application/json requests. |
| `pluginDescriptionForHumans` | body | `string` | no | PluginDescriptionForHumans for application/json requests. |
