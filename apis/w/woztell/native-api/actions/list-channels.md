# List Channels with Woztell

Retrieves channels from your Woztell workspace.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://open.api.woztell.com/v3`
- **Official documentation:** [List Channels](https://doc.woztell.com/open-api-reference/#query-apiViewer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables` | body | `object` | no | Optional GraphQL variables object. Supported keys include appId, first, after, before, channelIds, includeArchived, search, sortBy, and type. |
