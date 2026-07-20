# Get Member with Woztell

Retrieves a member from your Woztell workspace.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://open.api.woztell.com/v3`
- **Official documentation:** [Get Member](https://doc.woztell.com/docs/reference/open-api-reference/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables` | body | `object` | no | Optional GraphQL variables object. Supported keys include memberId, externalId, and channelId. Use channelId when resolving by externalId. |
