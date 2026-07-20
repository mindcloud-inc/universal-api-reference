# Create Channel with Woztell

Creates a channel in your Woztell workspace.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://open.api.woztell.com/v3`
- **Official documentation:** [Create Channel](https://doc.woztell.com/open-api-reference/#mutation-createChannel)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables` | body | `object` | yes | GraphQL variables object. Use {"input":{"name":"..."}} and optionally include description, tags, app, info, meta, or on from CreateChannelInput. |
