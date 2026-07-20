# <img src="https://images.mindcloud.co/apps/icons/thrivedesk-icon_1776704190550.png" alt="ThriveDesk logo" width="28" height="28"> ThriveDesk: Universal API

ThriveDesk is an AI helpdesk platform for shared inboxes, customer conversations, live chat assistants, knowledge bases, contacts, and billing/account data.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/thriveDesk/latest
- **Actions:** 143
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.thrivedesk.com
- **Vendor API docs:** https://developer.thrivedesk.com

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account](actions/get-account.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/thriveDesk/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (143)

### Access Token

| Action | Method | Description |
| --- | --- | --- |
| [Delete Access Token](actions/delete-access-token.md) | DELETE |  |

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | GET |  |

### Api Key

| Action | Method | Description |
| --- | --- | --- |
| [Create Company API Key](actions/create-company-api-key.md) | POST |  |
| [List Company API Keys](actions/list-company-api-keys.md) | GET |  |

### Api Root

| Action | Method | Description |
| --- | --- | --- |
| [Get API Root](actions/get-api-root.md) | GET |  |

### Api Version

| Action | Method | Description |
| --- | --- | --- |
| [Get API Version](actions/get-api-version.md) | GET |  |

### App

| Action | Method | Description |
| --- | --- | --- |
| [List Apps](actions/list-apps.md) | GET |  |

### App Installation

| Action | Method | Description |
| --- | --- | --- |
| [Install App](actions/install-app.md) | POST |  |

### Assistant

| Action | Method | Description |
| --- | --- | --- |
| [Create Assistant](actions/create-assistant.md) | POST |  |
| [Delete Assistant](actions/delete-assistant.md) | DELETE |  |
| [List Assistants](actions/list-assistants.md) | GET |  |
| [Update Assistant](actions/update-assistant.md) | PUT |  |

### Automation

| Action | Method | Description |
| --- | --- | --- |
| [Create Inbox Automation](actions/create-inbox-automation.md) | POST |  |
| [Delete Inbox Automation](actions/delete-inbox-automation.md) | DELETE |  |
| [Get Inbox Automation](actions/get-inbox-automation.md) | GET |  |
| [List Inbox Automations](actions/list-inbox-automations.md) | GET |  |
| [Update Inbox Automation](actions/update-inbox-automation.md) | PUT |  |

### Billing Feature

| Action | Method | Description |
| --- | --- | --- |
| [Get Billing Features](actions/get-billing-features.md) | GET |  |

### Billing Plan

| Action | Method | Description |
| --- | --- | --- |
| [Get Current Billing Plan](actions/get-current-billing-plan.md) | GET |  |

### Billing Receipt

| Action | Method | Description |
| --- | --- | --- |
| [List Billing Receipts](actions/list-billing-receipts.md) | GET |  |

### Community

| Action | Method | Description |
| --- | --- | --- |
| [Create Community](actions/create-community.md) | POST |  |
| [Delete Community](actions/delete-community.md) | DELETE |  |
| [Get Community](actions/get-community.md) | GET |  |
| [List Communities](actions/list-communities.md) | GET |  |
| [Update Community](actions/update-community.md) | PUT |  |

### Community Access

| Action | Method | Description |
| --- | --- | --- |
| [Get Community Access](actions/get-community-access.md) | GET |  |

### Company Settings

| Action | Method | Description |
| --- | --- | --- |
| [Get Company Settings](actions/get-company-settings.md) | GET |  |
| [Update Company Settings](actions/update-company-settings.md) | PUT |  |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST |  |
| [Get Contact](actions/get-contact.md) | GET |  |
| [List Contacts](actions/list-contacts.md) | GET |  |
| [Update Contact](actions/update-contact.md) | PUT |  |

### Conversation

| Action | Method | Description |
| --- | --- | --- |
| [Batch Delete Inbox Conversations](actions/batch-delete-inbox-conversations.md) | DELETE |  |
| [Batch Force Delete Inbox Conversations](actions/batch-force-delete-inbox-conversations.md) | DELETE |  |
| [Batch Restore Inbox Conversations](actions/batch-restore-inbox-conversations.md) | PUT |  |
| [Batch Update Inbox Conversations](actions/batch-update-inbox-conversations.md) | PUT |  |
| [Create Inbox Conversation](actions/create-inbox-conversation.md) | POST |  |
| [Delete Conversation](actions/delete-conversation.md) | DELETE |  |
| [Force Delete Conversation](actions/force-delete-conversation.md) | DELETE |  |
| [Get Conversation](actions/get-conversation.md) | GET |  |
| [Get Next Conversation](actions/get-next-conversation.md) | GET |  |
| [Get Previous Conversation](actions/get-previous-conversation.md) | GET |  |
| [List Contact Conversations](actions/list-contact-conversations.md) | GET |  |
| [List My Conversations](actions/list-my-conversations.md) | GET |  |
| [Merge Conversation](actions/merge-conversation.md) | PUT |  |
| [Move Conversation](actions/move-conversation.md) | PUT |  |
| [Restore Conversation](actions/restore-conversation.md) | PUT |  |
| [Save New Conversation](actions/save-new-conversation.md) | POST |  |
| [Update Conversation](actions/update-conversation.md) | PUT |  |
| [Update Conversation Priority](actions/update-conversation-priority.md) | PUT |  |
| [Update New Conversation](actions/update-new-conversation.md) | PUT |  |

### Conversation Draft

| Action | Method | Description |
| --- | --- | --- |
| [Create Conversation Draft](actions/create-conversation-draft.md) | POST |  |
| [Delete Conversation Draft](actions/delete-conversation-draft.md) | DELETE |  |
| [Take Over Conversation Draft](actions/take-over-conversation-draft.md) | PUT |  |

### Conversation Event

| Action | Method | Description |
| --- | --- | --- |
| [Retry Conversation Event](actions/retry-conversation-event.md) | PUT |  |

### Conversation Note

| Action | Method | Description |
| --- | --- | --- |
| [Create Conversation Note](actions/create-conversation-note.md) | POST |  |

### Conversation Reply

| Action | Method | Description |
| --- | --- | --- |
| [Reply To Conversation](actions/reply-to-conversation.md) | POST |  |
| [Reply To Customer Conversation](actions/reply-to-customer-conversation.md) | POST |  |

### Conversation Tag

| Action | Method | Description |
| --- | --- | --- |
| [Add Conversation Tags](actions/add-conversation-tags.md) | POST |  |
| [Remove Conversation Tags](actions/remove-conversation-tags.md) | DELETE |  |

### Customer Conversation

| Action | Method | Description |
| --- | --- | --- |
| [Get Customer Conversation](actions/get-customer-conversation.md) | GET |  |
| [List Customer Conversations](actions/list-customer-conversations.md) | GET |  |

### Inbox

| Action | Method | Description |
| --- | --- | --- |
| [Create Inbox Settings](actions/create-inbox-settings.md) | POST |  |
| [Delete Inbox Settings](actions/delete-inbox-settings.md) | DELETE |  |
| [Get Inbox](actions/get-inbox.md) | GET |  |
| [List Inboxes](actions/list-inboxes.md) | GET |  |
| [Update Inbox Settings](actions/update-inbox-settings.md) | PUT |  |

### Inbox Alias

| Action | Method | Description |
| --- | --- | --- |
| [Create Inbox Alias](actions/create-inbox-alias.md) | POST |  |
| [Delete Inbox Alias](actions/delete-inbox-alias.md) | DELETE |  |
| [List Inbox Aliases](actions/list-inbox-aliases.md) | GET |  |
| [Mark Inbox Alias Primary](actions/mark-inbox-alias-primary.md) | PUT |  |
| [Send Inbox Alias Verification Code](actions/send-inbox-alias-verification-code.md) | POST |  |
| [Validate Inbox Alias](actions/validate-inbox-alias.md) | GET |  |
| [Verify Inbox Alias Code](actions/verify-inbox-alias-code.md) | PUT |  |

### Inbox Alias Connection

| Action | Method | Description |
| --- | --- | --- |
| [Get Inbox Alias Connection](actions/get-inbox-alias-connection.md) | GET |  |

### Inbox Connection

| Action | Method | Description |
| --- | --- | --- |
| [Delete Inbox Connection](actions/delete-inbox-connection.md) | DELETE |  |
| [Get Inbox Connection](actions/get-inbox-connection.md) | GET |  |
| [Send Inbox Connection](actions/send-inbox-connection.md) | POST |  |
| [Test Inbox Connection](actions/test-inbox-connection.md) | GET |  |
| [Validate Inbox Connection](actions/validate-inbox-connection.md) | GET |  |
| [Verify Inbox Connection](actions/verify-inbox-connection.md) | PUT |  |

### Inbox Permission

| Action | Method | Description |
| --- | --- | --- |
| [Update Inbox Permissions](actions/update-inbox-permissions.md) | PUT |  |

### Installed App

| Action | Method | Description |
| --- | --- | --- |
| [List Installed Apps](actions/list-installed-apps.md) | GET |  |

### Invitation Organization

| Action | Method | Description |
| --- | --- | --- |
| [Get Invitation Organization](actions/get-invitation-organization.md) | GET |  |

### Knowledge Base

| Action | Method | Description |
| --- | --- | --- |
| [Create Knowledge Base](actions/create-knowledge-base.md) | POST |  |
| [Delete Knowledge Base](actions/delete-knowledge-base.md) | DELETE |  |
| [Get Knowledge Base](actions/get-knowledge-base.md) | GET |  |
| [List Knowledge Bases](actions/list-knowledge-bases.md) | GET |  |
| [Update Knowledge Base](actions/update-knowledge-base.md) | PUT |  |

### Knowledge Base Access

| Action | Method | Description |
| --- | --- | --- |
| [Get Knowledge Base Access](actions/get-knowledge-base-access.md) | GET |  |

### Knowledge Base User

| Action | Method | Description |
| --- | --- | --- |
| [Add Knowledge Base User](actions/add-knowledge-base-user.md) | POST |  |
| [List Knowledge Base Users](actions/list-knowledge-base-users.md) | GET |  |

### Login Session

| Action | Method | Description |
| --- | --- | --- |
| [List User Login Sessions](actions/list-user-login-sessions.md) | GET |  |

### Notification

| Action | Method | Description |
| --- | --- | --- |
| [List Live Chat Notifications](actions/list-live-chat-notifications.md) | GET |  |
| [List Notifications](actions/list-notifications.md) | GET |  |
| [Mark Live Chat Notification Read](actions/mark-live-chat-notification-read.md) | PUT |  |
| [Mark Notification Read](actions/mark-notification-read.md) | PUT |  |
| [Mark Notifications Read](actions/mark-notifications-read.md) | PUT |  |

### Notification Preference

| Action | Method | Description |
| --- | --- | --- |
| [Update Notification Preferences](actions/update-notification-preferences.md) | PUT |  |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [Create Organization](actions/create-organization.md) | POST |  |
| [Delete Organization](actions/delete-organization.md) | DELETE |  |
| [Switch Organization](actions/switch-organization.md) | PUT |  |

### Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Agent Team Conversation Report](actions/get-agent-team-conversation-report.md) | GET |  |
| [Get Agent Team Productivity Report](actions/get-agent-team-productivity-report.md) | GET |  |
| [Get Agents Report](actions/get-agents-report.md) | GET |  |
| [Get Conversations Report](actions/get-conversations-report.md) | GET |  |
| [Get Happiness Report](actions/get-happiness-report.md) | GET |  |
| [Get Inbox Reports](actions/get-inbox-reports.md) | GET |  |
| [Get Productivity Report](actions/get-productivity-report.md) | GET |  |
| [List Recent Rating Report](actions/list-recent-rating-report.md) | GET |  |

### Satisfaction Rating Setting

| Action | Method | Description |
| --- | --- | --- |
| [Reset Inbox Satisfaction Ratings](actions/reset-inbox-satisfaction-ratings.md) | PUT |  |
| [Update Inbox Satisfaction Ratings](actions/update-inbox-satisfaction-ratings.md) | PUT |  |

### Saved Reply

| Action | Method | Description |
| --- | --- | --- |
| [Create Saved Reply](actions/create-saved-reply.md) | POST |  |
| [Delete Saved Reply](actions/delete-saved-reply.md) | DELETE |  |
| [List Inbox Saved Replies](actions/list-inbox-saved-replies.md) | GET |  |
| [List Saved Replies](actions/list-saved-replies.md) | GET |  |
| [Update Saved Reply](actions/update-saved-reply.md) | PUT |  |
| [Use Saved Reply](actions/use-saved-reply.md) | PUT |  |

### Saved Reply Folder

| Action | Method | Description |
| --- | --- | --- |
| [Delete Saved Reply Folder](actions/delete-saved-reply-folder.md) | DELETE |  |
| [Update Saved Reply Folder](actions/update-saved-reply-folder.md) | PUT |  |

### Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Search](actions/search.md) | GET |  |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Delete Settings Tags](actions/bulk-delete-settings-tags.md) | DELETE |  |
| [Bulk Update Settings Tags](actions/bulk-update-settings-tags.md) | PUT |  |
| [Create Settings Tag](actions/create-settings-tag.md) | POST |  |
| [Delete Settings Tag](actions/delete-settings-tag.md) | DELETE |  |
| [List Inbox Tags](actions/list-inbox-tags.md) | GET |  |
| [List Settings Tags](actions/list-settings-tags.md) | GET |  |
| [Merge Settings Tags](actions/merge-settings-tags.md) | PUT |  |
| [Update Settings Tag](actions/update-settings-tag.md) | PUT |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Delete Settings User](actions/delete-settings-user.md) | DELETE |  |
| [Get Settings User](actions/get-settings-user.md) | GET |  |
| [List Settings Users](actions/list-settings-users.md) | GET |  |
| [Remove Settings User](actions/remove-settings-user.md) | DELETE |  |
| [Send User Password Reset](actions/send-user-password-reset.md) | POST |  |
| [Update Settings User](actions/update-settings-user.md) | PUT |  |
| [Validate Settings User](actions/validate-settings-user.md) | GET |  |

### User Invitation

| Action | Method | Description |
| --- | --- | --- |
| [Accept User Invitation](actions/accept-user-invitation.md) | POST |  |
| [Cancel User Invitation](actions/cancel-user-invitation.md) | DELETE |  |
| [Create User Invitation](actions/create-user-invitation.md) | POST |  |
| [Decline User Invitation](actions/decline-user-invitation.md) | DELETE |  |

### User Permission

| Action | Method | Description |
| --- | --- | --- |
| [Get User Permissions](actions/get-user-permissions.md) | GET |  |
| [Update User Permissions](actions/update-user-permissions.md) | PUT |  |

### User Role

| Action | Method | Description |
| --- | --- | --- |
| [Update User Role](actions/update-user-role.md) | PUT |  |

