# Api to update message from conversation with Kite Suite

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/chat/:id`
- **Base URL:** `https://api.kitesuite.com`
- **Official documentation:** [Api to update message from conversation](https://api.kitesuite.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | yes | Request body |
| `id` | path | `string` | no | Message Id |
| `message` | body | `string` | yes | — |
| `taggedUsers[]` | body | `array` | yes | — |
| `reaction` | body | `string` | yes | — |
| `reactionName` | body | `string` | yes | — |
