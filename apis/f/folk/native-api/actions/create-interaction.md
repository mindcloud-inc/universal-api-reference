# Create Interaction with folk

Creates an interaction for a person or company in folk.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/interactions`
- **Base URL:** `https://api.folk.app`
- **Official documentation:** [Create Interaction](https://developer.folk.app/api-reference/interactions/create-an-interaction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entity.id` | body | `string` | yes | The ID of the person or company connected to the interaction. |
| `dateTime` | body | `string` | yes | The date and time of the interaction in ISO 8601 format. |
| `title` | body | `string` | yes | The title of the interaction. |
| `content` | body | `string` | yes | The multi-line content of the interaction. |
| `type` | body | `string` | yes | An emoji or supported type token representing the interaction type. |
