# Check if a conversation exists with a profile with ConnectSafely

Check whether the authenticated LinkedIn account already has an existing conversation with a target profile. Returns the conversation URN if one exists. Single LinkedIn API call (no message history fetched). Useful as a precheck before sending a connection request or message to avoid duplicate outreach.

## Endpoint

- **Method:** `GET`
- **Path:** `/conversations/exists/:profileId`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [Check if a conversation exists with a profile](https://connectsafely.ai/docs/api/linkedin-messaging/get-conversations-exists-profileid-conversation-exists)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `profileId` | param | `string` | yes | LinkedIn profile vanity URL slug (the part after linkedin.com/in/, e.g., "john-doe-123") |
| `accountId` | query | `string` | no | LinkedIn account ID to check from. Omit to use the default account for the authenticated user. |

## Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | `boolean` |  |
| `hasConversation` | `boolean` | Whether a conversation already exists with this profile |
| `conversationUrn` | `string` | Existing conversation URN if one exists, otherwise null |
| `profileUrn` | `string` | Resolved LinkedIn profile URN of the target user |
| `accountId` | `string` | LinkedIn account ID used for the check |

## Error status codes

`401`, `404`, `500`. Bodies follow the shared `{ success, code, message }` error shape.
