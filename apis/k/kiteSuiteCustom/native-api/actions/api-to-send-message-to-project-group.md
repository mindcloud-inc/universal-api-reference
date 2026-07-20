# Api to send message to Project Group with Kite Suite

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/chat`
- **Base URL:** `https://api.kitesuite.com`
- **Official documentation:** [Api to send message to Project Group](https://api.kitesuite.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | yes | Request body |
| `conversationID` | body | `string` | yes | — |
| `message` | body | `string` | yes | — |
| `taggedMessage` | body | `string` | yes | — |
| `taggedUsers[]` | body | `array` | yes | — |
| `files[]` | body | `array` | yes | — |
