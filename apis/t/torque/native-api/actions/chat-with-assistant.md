# Chat With Assistant with Torque

## Endpoint

- **Method:** `POST`
- **Path:** `/assistant/chat`
- **Base URL:** `https://app.torque.fi/api`
- **Official documentation:** [Chat With Assistant](https://docs.torque.fi/business/api-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `messages[]` | body | `array<object>` | yes | Conversation messages with role and content. |
| `context` | body | `object` | no | Optional assistant context such as walletAddress, chainId, localCurrency, or portfolioData. |
| `conversationId` | body | `string` | no | Optional conversation ID for continuity. |
