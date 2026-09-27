# Send message (with channel selection) with ConnectSafely

Send a LinkedIn message. By default, messagingChannel is "auto" which auto-detects whether to use Sales Navigator or standard LinkedIn inbox based on the account premium status. Users can explicitly control the messaging channel by setting messagingChannel to: "sales_navigator" — forces the message through the Sales Navigator API (returns a 400 error if the account does not have an active Sales Navigator subscription), or "linkedin_inbox" — forces standard LinkedIn messaging even if the account has Sales Navigator. Example: to send via standard inbox on a Sales Nav account, pass { "messagingChannel": "linkedin_inbox" }. To explicitly use Sales Navigator, pass { "messagingChannel": "sales_navigator" }. If omitted or set to "auto", the system decides automatically. **File attachments:** first upload each file via POST /conversations/upload-attachment, then pass each returned attachment object in the `attachments` array, each wrapped in a `file` key — `{ "attachments": [{ "file": { "assetUrn": "...", "byteSize": 123, "mediaType": "image/png", "name": "photo.png" } }] }`. An attachment whose file was uploaded with an image/* content type renders inline as a photo; anything else renders as a downloadable file. **Rate limit: 150 NEW conversations per day per LinkedIn account** (resets at midnight UTC). The quota applies to cold outreach only — a message that starts a conversation with someone this account has no existing thread with. Replying inside an existing conversation is unlimited, whether you pass `conversationUrn` or a recipient this account has already messaged. Over-quota cold sends return 429 with `X-RateLimit-Limit`, `X-RateLimit-Remaining` and `X-RateLimit-Reset` headers, and are rejected before any LinkedIn request is made.

## Endpoint

- **Method:** `POST`
- **Path:** `/conversations/send`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [Send message (with channel selection)](https://connectsafely.ai/docs/api/linkedin-messaging/post-conversations-send-conversations-send-message)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | body | `string` | no | LinkedIn account ID |
| `recipientProfileId` | body | `string` | no | Recipient LinkedIn profile vanity URL slug (e.g., "john-doe-123"). Prefer recipientProfileUrn when available. |
| `recipientProfileUrn` | body | `string` | no | Recipient LinkedIn profile URN (e.g., "urn:li:fsd_profile:ACoAABJefVoBrz2LR3f..."). Preferred over recipientProfileId. |
| `conversationUrn` | body | `string` | no | Existing conversation URN (skips recipient lookup) |
| `message` | body | `string` | yes | Message text |
| `subject` | body | `string` | no | Message subject (optional) |
| `attachments` | body | `array` | no | File attachments from the upload-attachment endpoint. Each item must wrap the upload response in a `file` key: [{ "file": { assetUrn, byteSize, mediaType, name } }]. Files uploaded with an image/* content type render inline as photos; others render as downloadable files. |
| `messagingChannel` | body | `list` | no | Controls which messaging channel to use. Defaults to "auto" if not provided. Options: "auto" — automatically detects the best channel based on account premium status (Sales Navigator accounts use Sales Nav API, others use standard inbox). "sales_navigator" — explicitly send via Sales Navigator API. Use this when the user wants to send through Sales Navigator. Returns a 400 error with a clear message if the account does not have Sales Navigator. "linkedin_inbox" — explicitly send via standard LinkedIn inbox. Use this when the user wants to bypass Sales Navigator and send through the regular LinkedIn messaging, even if the account has a Sales Navigator subscription. Accepted values: `auto`, `sales_navigator`, `linkedin_inbox`. Default: `auto`. |

## Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | `boolean` |  |
| `message` | `string` |  |
| `recipientProfileUrn` | `string` |  |
| `sentMessage` | `object` |  |
| `sentMessage.messageUrn` | `string` |  |
| `sentMessage.text` | `string` |  |
| `sentMessage.sentAt` | `number` |  |
| `sentMessage.senderProfileId` | `string` |  |
| `sentMessage.senderName` | `string` |  |
| `sentMessage.senderPhoto` | `string` |  |
| `sentMessage.isSentByOwner` | `boolean` |  |
| `threadId` | `string` | Sales Navigator thread ID (only for Sales Nav accounts) |

## Error status codes

`400`, `401`, `404`, `500`. Bodies follow the shared `{ success, code, message }` error shape.
