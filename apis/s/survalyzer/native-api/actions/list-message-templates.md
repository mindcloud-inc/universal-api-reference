# List Message Templates with Survalyzer

## Endpoint

- **Method:** `POST`
- **Path:** `/publicapi/Distribute/v3/ReadMessageTemplateList`
- **Base URL:** `https://api.survalyzer-eu.app`
- **Official documentation:** [List Message Templates](https://developer.survalyzer.com/knowledge-base/public-api-eu/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | body | `number` | no | Workspace identifier that owns the message templates. |
| `language` | body | `string` | yes | Language code for the message templates. |
