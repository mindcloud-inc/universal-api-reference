# <img src="https://images.mindcloud.co/apps/icons/wbiztool_1773852472205.png" alt="Wbiztool logo" width="28" height="28"> Wbiztool: Universal API

Send, schedule, and automate WhatsApp business messages

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/wbiztool/latest
- **Category:** Communication / Team Messaging
- **Actions:** 23
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://wbiztool.com/
- **Vendor API docs:** https://wbiztool.com/docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Check Credentials](actions/check-credentials.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wbiztool/latest/actions/check-credentials?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (23)

### Connection

| Action | Method | Description |
| --- | --- | --- |
| [Check Credentials](actions/check-credentials.md) | GET | Checks whether your Wbiztool credentials are valid. |

### Media File

| Action | Method | Description |
| --- | --- | --- |
| [Get Media File](actions/get-media-file.md) | GET | Retrieves a specific media file from Wbiztool. |
| [List Media Files](actions/list-media-files.md) | GET | Retrieves media files from Wbiztool. |
| [Upload Media](actions/upload-media.md) | POST | Uploads a media file to Wbiztool. |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Message](actions/cancel-message.md) | DELETE | Cancels a scheduled or queued message in Wbiztool. |
| [Get Message Status](actions/get-message-status.md) | GET | Retrieves WhatsApp message delivery status from Wbiztool. |
| [List Message History](actions/list-message-history.md) | GET | Retrieves WhatsApp message history from Wbiztool. |
| [Schedule File Message](actions/schedule-file-message.md) | POST | Creates a scheduled WhatsApp file message in Wbiztool. |
| [Schedule Image Message](actions/schedule-image-message.md) | POST | Creates a scheduled WhatsApp image message in Wbiztool. |
| [Schedule Text Message](actions/schedule-text-message.md) | POST | Creates a scheduled WhatsApp text message in Wbiztool. |
| [Send File Message](actions/send-file-message.md) | POST | Creates a WhatsApp file message in Wbiztool. |
| [Send Image Message](actions/send-image-message.md) | POST | Creates a WhatsApp image message in Wbiztool. |
| [Send Multi Messages](actions/send-multi-messages.md) | POST | Creates WhatsApp messages for multiple recipients in Wbiztool. |
| [Send Text Message](actions/send-text-message.md) | POST | Creates a WhatsApp text message in Wbiztool. |

### Reminder

| Action | Method | Description |
| --- | --- | --- |
| [Create Reminder](actions/create-reminder.md) | POST | Creates a recurring WhatsApp reminder in Wbiztool. |
| [List Reminders](actions/list-reminders.md) | GET | Retrieves active reminders from Wbiztool. |

### Verification Campaign

| Action | Method | Description |
| --- | --- | --- |
| [Create Verification Campaign](actions/create-verification-campaign.md) | POST | Creates a WhatsApp number verification campaign in Wbiztool. |
| [Get Verification Status](actions/get-verification-status.md) | GET | Retrieves verification campaign status from Wbiztool. |
| [List Verification Results](actions/list-verification-results.md) | GET | Retrieves verification results for a campaign in Wbiztool. |

### Whatsapp Account

| Action | Method | Description |
| --- | --- | --- |
| [Connect WhatsApp Number](actions/connect-whats-app-number.md) | POST | Connects a WhatsApp account in Wbiztool. |
| [Get Current WhatsApp Client Status](actions/get-current-whats-app-client-status.md) | GET | Retrieves the current WhatsApp client status from Wbiztool. |
| [Get WhatsApp Client Status By Id](actions/get-whats-app-client-status-by-id.md) | GET | Retrieves a specific WhatsApp client status by ID from Wbiztool. |
| [List WhatsApp Accounts](actions/list-whats-app-accounts.md) | GET | Retrieves WhatsApp client accounts from Wbiztool. |

