# Import Typebot with Typebot

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/typebots/import`
- **Base URL:** `https://app.typebot.io/api`
- **Official documentation:** [Import Typebot](https://docs.typebot.io/api-reference/typebot/import)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | body | `string` | yes | Workspace ID where the typebot should be imported. |
| `typebot` | body | `object` | yes | Typebot object payload to import. |
| `fromTemplate` | body | `string` | no | Optional template source identifier. |
| `enableSafetyFlags` | body | `boolean` | no | Whether to enable Typebot safety flags during import. |
