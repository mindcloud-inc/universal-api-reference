# Create Typebot with Typebot

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/typebots`
- **Base URL:** `https://app.typebot.io/api`
- **Official documentation:** [Create Typebot](https://docs.typebot.io/api-reference/typebot/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | body | `string` | yes | Workspace ID where the typebot should be created. |
| `typebot` | body | `object` | yes | Typebot object payload to create. |
