# Edit Inbox Conversation Note with LaGrowthMachine

Updates an inbox conversation note in LaGrowthMachine.

## Endpoint

- **Method:** `POST`
- **Path:** `/inbox/conversations/note`
- **Base URL:** `https://apiv2.lagrowthmachine.com/flow`
- **Official documentation:** [Edit Inbox Conversation Note](https://documenter.getpostman.com/view/2071164/TVCmSkH2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignId` | body | `string` | no | Optional campaign filter when resolving the conversation. |
| `campaignName` | body | `string` | no | Optional campaign-name filter when resolving the conversation. |
| `conversationId` | body | `string` | no | Conversation ID. Fastest and most reliable identifier when available. |
| `email` | body | `string` | no | Lead email used to resolve the conversation. |
| `identityId` | body | `string` | no | Optional identity filter when resolving the conversation. |
| `leadId` | body | `string` | no | Lead ID used to resolve the conversation. |
| `linkedinUrl` | body | `string` | no | Lead LinkedIn URL used to resolve the conversation. |
| `mode` | body | `string` | no | Either `replace` or `append`. |
| `note` | body | `string` | yes | Note content to store on the conversation. |
