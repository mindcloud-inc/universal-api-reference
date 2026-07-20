# List WhatsApp Numbers with 2Chat

Retrieves connected WhatsApp numbers from 2Chat.

## Endpoint

- **Method:** `GET`
- **Path:** `/whatsapp/get-numbers`
- **Base URL:** `https://api.p.2chat.io/open`
- **Official documentation:** [List WhatsApp Numbers](https://developers.2chat.co/docs/API/WhatsApp/Web/list-numbers)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `status` | query | `string` | no | Filter numbers by status: connected, disconnected, or all. |
