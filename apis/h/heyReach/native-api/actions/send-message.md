# Send Message with Hey Reach

Sends a message to a LinkedIn conversation in Hey Reach.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/public/inbox/SendMessage`
- **Base URL:** `https://api.heyreach.io`
- **Official documentation:** [Send Message](https://documenter.getpostman.com/view/23808049/2sA2xb5F75)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `message` | body | `string` | yes |
| `subject` | body | `string` | no |
| `conversationId` | body | `string` | yes |
| `linkedInAccountId` | body | `number` | yes |
