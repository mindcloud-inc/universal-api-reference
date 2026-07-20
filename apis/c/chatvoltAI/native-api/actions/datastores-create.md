# Create Datastore with Chatvolt AI

Creates a datastore in Chatvolt AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/datastores`
- **Base URL:** `https://api.chatvolt.ai`
- **Official documentation:** [Create Datastore](https://docs.chatvolt.ai/api-reference/endpoint/datastores/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | Datastore name. If not provided, a fun name will be generated automatically. |
| `description` | body | `string` | no | Datastore description. |
| `type` | body | `string` | yes | Datastore type (e.g., 'qdrant'). |
| `isPublic` | body | `boolean` | no | Defines whether the datastore is public (accessible without specific datastore authentication) or private. |
| `pluginName` | body | `string` | no | Short name for the OpenAI plugin associated with this datastore (optional, used if the datastore is exposed as a plugin). Maximum of 20 characters. |
| `pluginDescriptionForHumans` | body | `string` | no | Human-readable description for the OpenAI plugin (optional). Maximum of 90 characters. |
