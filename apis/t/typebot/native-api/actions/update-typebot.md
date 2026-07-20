# Update Typebot with Typebot

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/typebots/:typebotId`
- **Base URL:** `https://app.typebot.io/api`
- **Official documentation:** [Update Typebot](https://docs.typebot.io/api-reference/typebot/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `typebotId` | path | `string` | yes | Typebot ID to update. |
| `typebot` | body | `object` | yes | Typebot object payload to update. |
| `overwrite` | body | `boolean` | no | If true, updates are pushed even when a conflict is detected. |
