# ThriveDesk: Native API Reference

A consolidated summary of ThriveDesk's API configuration and 143 documented operations, with links to official documentation.

- **Official docs:** https://developer.thrivedesk.com
- **API base URL:** `https://api.thrivedesk.com`

## Authentication

### API Key

Use a ThriveDesk API key. ThriveDesk expects it as a bearer token in the Authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.thrivedesk.com/en/wpportal)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `per-page` in the query string to set the page size (default 25; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Retry behavior

Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (143 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Accept User Invitation](actions/accept-user-invitation.md) | `POST /v1/settings/users/invitation/{{token}}/accept` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Add Conversation Tags](actions/add-conversation-tags.md) | `POST /v1/conversation/{{conversationId}}/tags` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Add Knowledge Base User](actions/add-knowledge-base-user.md) | `POST /v1/knowledgebases/{{knowledgebaseId}}/users` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Batch Delete Inbox Conversations](actions/batch-delete-inbox-conversations.md) | `POST /v1/inboxes/{{inboxId}}/batch/delete` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Batch Force Delete Inbox Conversations](actions/batch-force-delete-inbox-conversations.md) | `POST /v1/inboxes/{{inboxId}}/batch/force-delete` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Batch Restore Inbox Conversations](actions/batch-restore-inbox-conversations.md) | `POST /v1/inboxes/{{inboxId}}/batch/restore` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Batch Update Inbox Conversations](actions/batch-update-inbox-conversations.md) | `POST /v1/inboxes/{{inboxId}}/batch/update` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Bulk Delete Settings Tags](actions/bulk-delete-settings-tags.md) | `POST /v1/settings/tags/delete` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Bulk Update Settings Tags](actions/bulk-update-settings-tags.md) | `POST /v1/settings/tags/update` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Cancel User Invitation](actions/cancel-user-invitation.md) | `DELETE /v1/settings/users/invitation/{{invitationId}}/cancel` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Create Assistant](actions/create-assistant.md) | `POST /v1/assistants` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Create Community](actions/create-community.md) | `POST /v1/communities` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Create Company API Key](actions/create-company-api-key.md) | `POST /v1/settings/company/api-keys` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Create Contact](actions/create-contact.md) | `POST /v1/contacts` | [docs](https://wordpress.org/plugins/thrivedesk/) |
| [Create Conversation Draft](actions/create-conversation-draft.md) | `POST /v1/conversation/{{conversationId}}/draft` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Create Conversation Note](actions/create-conversation-note.md) | `POST /v1/conversation/{{conversationId}}/note` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Create Inbox Alias](actions/create-inbox-alias.md) | `POST /v1/settings/inbox/{{inboxId}}/aliases` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Create Inbox Automation](actions/create-inbox-automation.md) | `POST /v1/inboxes/{{inboxId}}/automations` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Create Inbox Conversation](actions/create-inbox-conversation.md) | `POST /v1/inboxes/{{inboxId}}/conversations` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Create Inbox Settings](actions/create-inbox-settings.md) | `POST /v1/settings/inbox` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Create Knowledge Base](actions/create-knowledge-base.md) | `POST /v1/knowledgebases` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Create Organization](actions/create-organization.md) | `POST /v1/organizations` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Create Saved Reply](actions/create-saved-reply.md) | `POST /v1/saved-replies` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Create Settings Tag](actions/create-settings-tag.md) | `POST /v1/settings/tags` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Create User Invitation](actions/create-user-invitation.md) | `POST /v1/settings/users/invitation` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Decline User Invitation](actions/decline-user-invitation.md) | `DELETE /v1/settings/users/invitation/{{token}}/decline` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Delete Access Token](actions/delete-access-token.md) | `DELETE /v1/settings/access-tokens/{{tokenId}}` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Delete Assistant](actions/delete-assistant.md) | `DELETE /v1/assistants/{{assistantId}}` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Delete Community](actions/delete-community.md) | `DELETE /v1/communities/{{communityId}}` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Delete Conversation](actions/delete-conversation.md) | `DELETE /v1/conversation/{{conversationId}}` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Delete Conversation Draft](actions/delete-conversation-draft.md) | `POST /v1/conversation/{{conversationId}}/draft/delete` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Delete Inbox Alias](actions/delete-inbox-alias.md) | `DELETE /v1/settings/inbox/{{inboxId}}/aliases/{{aliasId}}` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Delete Inbox Automation](actions/delete-inbox-automation.md) | `DELETE /v1/inboxes/{{inboxId}}/automations/{{automationId}}` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Delete Inbox Connection](actions/delete-inbox-connection.md) | `DELETE /v1/settings/inbox/{{inboxId}}/connection` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Delete Inbox Settings](actions/delete-inbox-settings.md) | `DELETE /v1/settings/inbox/{{inboxId}}` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Delete Knowledge Base](actions/delete-knowledge-base.md) | `DELETE /v1/knowledgebases/{{knowledgebaseId}}` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Delete Organization](actions/delete-organization.md) | `DELETE /v1/organizations/{{organizationId}}` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Delete Saved Reply](actions/delete-saved-reply.md) | `DELETE /v1/saved-replies/{{savedReplyId}}` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Delete Saved Reply Folder](actions/delete-saved-reply-folder.md) | `POST /v1/saved-replies/folder/delete` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Delete Settings Tag](actions/delete-settings-tag.md) | `DELETE /v1/settings/tags/{{tagId}}` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Delete Settings User](actions/delete-settings-user.md) | `POST /v1/settings/users/{{userId}}/delete` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Force Delete Conversation](actions/force-delete-conversation.md) | `DELETE /v1/conversation/{{conversationId}}/force-delete` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Get Account](actions/get-account.md) | `GET /v1/me` | [docs](https://help.thrivedesk.com/en/wpportal) |
| [Get Agent Team Conversation Report](actions/get-agent-team-conversation-report.md) | `GET /v1/reports/{{inboxId}}/agent-team-conversations` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Get Agent Team Productivity Report](actions/get-agent-team-productivity-report.md) | `GET /v1/reports/{{inboxId}}/agent-team-productivity` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Get Agents Report](actions/get-agents-report.md) | `GET /v1/reports/{{inboxId}}/agents` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Get API Root](actions/get-api-root.md) | `GET /` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Get API Version](actions/get-api-version.md) | `GET /v1` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Get Billing Features](actions/get-billing-features.md) | `GET /v1/billing/features` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Get Community](actions/get-community.md) | `GET /v1/communities/{{communityId}}` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Get Community Access](actions/get-community-access.md) | `GET /v1/communities/{{communityId}}/access` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Get Company Settings](actions/get-company-settings.md) | `GET /v1/settings/company` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Get Contact](actions/get-contact.md) | `GET /v1/contacts/{{contactId}}` | [docs](https://wordpress.org/plugins/thrivedesk/) |
| [Get Conversation](actions/get-conversation.md) | `GET /v1/conversation/{{conversationId}}` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Get Conversations Report](actions/get-conversations-report.md) | `GET /v1/reports/{{inboxId}}/conversations` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Get Current Billing Plan](actions/get-current-billing-plan.md) | `GET /v1/billing/plans/current` | [docs](https://help.thrivedesk.com/en/wpportal) |
| [Get Customer Conversation](actions/get-customer-conversation.md) | `GET /v1/customer/conversations/{{conversationId}}` | [docs](https://help.thrivedesk.com/en/wpportal) |
| [Get Happiness Report](actions/get-happiness-report.md) | `GET /v1/reports/{{inboxId}}/happiness` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Get Inbox](actions/get-inbox.md) | `GET /v1/inboxes/{{inboxId}}` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Get Inbox Alias Connection](actions/get-inbox-alias-connection.md) | `GET /v1/settings/inbox/{{inboxId}}/aliases/{{aliasId}}/connection` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Get Inbox Automation](actions/get-inbox-automation.md) | `GET /v1/inboxes/{{inboxId}}/automations/{{automationId}}` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Get Inbox Connection](actions/get-inbox-connection.md) | `GET /v1/settings/inbox/{{inboxId}}/connection` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Get Inbox Reports](actions/get-inbox-reports.md) | `GET /v1/inboxes/{{inboxId}}/reports` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Get Invitation Organization](actions/get-invitation-organization.md) | `GET /v1/settings/users/invitation/{{token}}/organization` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Get Knowledge Base](actions/get-knowledge-base.md) | `GET /v1/knowledgebases/{{knowledgebaseId}}` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Get Knowledge Base Access](actions/get-knowledge-base-access.md) | `GET /v1/knowledgebases/{{knowledgebaseId}}/access` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Get Next Conversation](actions/get-next-conversation.md) | `GET /v1/conversation/{{conversationId}}/next` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Get Previous Conversation](actions/get-previous-conversation.md) | `GET /v1/conversation/{{conversationId}}/previous` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Get Productivity Report](actions/get-productivity-report.md) | `GET /v1/reports/{{inboxId}}/productivity` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Get Settings User](actions/get-settings-user.md) | `GET /v1/settings/users/{{userId}}` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Get User Permissions](actions/get-user-permissions.md) | `GET /v1/settings/users/{{userId}}/permissions` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Install App](actions/install-app.md) | `POST /v1/apps/{{appNamespace}}/install` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [List Apps](actions/list-apps.md) | `GET /v1/apps` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [List Assistants](actions/list-assistants.md) | `GET /v1/assistants` | [docs](https://developer.thrivedesk.com/assistant/assistant-for-web) |
| [List Billing Receipts](actions/list-billing-receipts.md) | `GET /v1/billing/receipts` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [List Communities](actions/list-communities.md) | `GET /v1/communities` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [List Company API Keys](actions/list-company-api-keys.md) | `GET /v1/settings/company/api-keys` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [List Contact Conversations](actions/list-contact-conversations.md) | `GET /v1/contacts/{{contactId}}/conversations` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [List Contacts](actions/list-contacts.md) | `GET /v1/contacts` | [docs](https://wordpress.org/plugins/thrivedesk/) |
| [List Customer Conversations](actions/list-customer-conversations.md) | `GET /v1/customer/conversations` | [docs](https://help.thrivedesk.com/en/wpportal) |
| [List Inbox Aliases](actions/list-inbox-aliases.md) | `GET /v1/settings/inbox/{{inboxId}}/aliases` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [List Inbox Automations](actions/list-inbox-automations.md) | `GET /v1/inboxes/{{inboxId}}/automations` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [List Inbox Saved Replies](actions/list-inbox-saved-replies.md) | `GET /v1/inboxes/{{inboxId}}/saved-replies` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [List Inbox Tags](actions/list-inbox-tags.md) | `GET /v1/inboxes/{{inboxId}}/tags` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [List Inboxes](actions/list-inboxes.md) | `GET /v1/inboxes` | [docs](https://help.thrivedesk.com/en/wpportal) |
| [List Installed Apps](actions/list-installed-apps.md) | `GET /v1/installed-apps` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [List Knowledge Base Users](actions/list-knowledge-base-users.md) | `GET /v1/knowledgebases/{{knowledgebaseId}}/users` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [List Knowledge Bases](actions/list-knowledge-bases.md) | `GET /v1/knowledgebases` | [docs](https://help.thrivedesk.com/en/add-assistant-to-wordpress) |
| [List Live Chat Notifications](actions/list-live-chat-notifications.md) | `GET /v1/live_chat/notifications` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [List My Conversations](actions/list-my-conversations.md) | `GET /v1/conversations/mine` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [List Notifications](actions/list-notifications.md) | `GET /v1/notifications` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [List Recent Rating Report](actions/list-recent-rating-report.md) | `GET /v1/reports/{{inboxId}}/recent-ratings` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [List Saved Replies](actions/list-saved-replies.md) | `GET /v1/saved-replies` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [List Settings Tags](actions/list-settings-tags.md) | `GET /v1/settings/tags` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [List Settings Users](actions/list-settings-users.md) | `GET /v1/settings/users` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [List User Login Sessions](actions/list-user-login-sessions.md) | `GET /v1/settings/users/login-sessions` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Mark Inbox Alias Primary](actions/mark-inbox-alias-primary.md) | `PATCH /v1/settings/inbox/{{inboxId}}/aliases/{{aliasId}}/mark-as-primary` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Mark Live Chat Notification Read](actions/mark-live-chat-notification-read.md) | `PATCH /v1/live_chat/notifications/{{notificationId}}/read` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Mark Notification Read](actions/mark-notification-read.md) | `PATCH /v1/notifications/{{notificationId}}/read` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Mark Notifications Read](actions/mark-notifications-read.md) | `PATCH /v1/notifications/read` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Merge Conversation](actions/merge-conversation.md) | `POST /v1/conversation/{{conversationId}}/merge` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Merge Settings Tags](actions/merge-settings-tags.md) | `POST /v1/settings/tags/merge` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Move Conversation](actions/move-conversation.md) | `POST /v1/conversation/{{conversationId}}/move` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Remove Conversation Tags](actions/remove-conversation-tags.md) | `DELETE /v1/conversation/{{conversationId}}/tags` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Remove Settings User](actions/remove-settings-user.md) | `POST /v1/settings/users/{{userId}}/remove` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Reply To Conversation](actions/reply-to-conversation.md) | `POST /v1/conversation/{{conversationId}}/reply` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Reply To Customer Conversation](actions/reply-to-customer-conversation.md) | `POST /v1/customer/conversations/{{conversationId}}/reply` | [docs](https://help.thrivedesk.com/en/wpportal) |
| [Reset Inbox Satisfaction Ratings](actions/reset-inbox-satisfaction-ratings.md) | `POST /v1/settings/inbox/{{inboxId}}/satisfaction-ratings/reset` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Restore Conversation](actions/restore-conversation.md) | `PATCH /v1/conversation/{{conversationId}}/restore` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Retry Conversation Event](actions/retry-conversation-event.md) | `POST /v1/conversations/{{conversationId}}/events/{{eventId}}/retry` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Save New Conversation](actions/save-new-conversation.md) | `POST /v1/conversation/{{conversationId}}/save-new-conversation` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Search](actions/search.md) | `POST /v1/search` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Send Inbox Alias Verification Code](actions/send-inbox-alias-verification-code.md) | `POST /v1/settings/inbox/{{inboxId}}/aliases/{{aliasId}}/send-code` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Send Inbox Connection](actions/send-inbox-connection.md) | `POST /v1/settings/inbox/{{inboxId}}/connection/send` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Send User Password Reset](actions/send-user-password-reset.md) | `POST /v1/settings/users/{{userId}}/password/reset` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Switch Organization](actions/switch-organization.md) | `POST /v1/organizations/switch` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Take Over Conversation Draft](actions/take-over-conversation-draft.md) | `POST /v1/conversation/{{conversationId}}/draft/{{eventId}}/take-over` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Test Inbox Connection](actions/test-inbox-connection.md) | `POST /v1/settings/inbox/{{inboxId}}/connection/test` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Update Assistant](actions/update-assistant.md) | `PUT /v1/assistants/{{assistantId}}` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Update Community](actions/update-community.md) | `POST /v1/communities/{{communityId}}` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Update Company Settings](actions/update-company-settings.md) | `PUT /v1/settings/company` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Update Contact](actions/update-contact.md) | `PATCH /v1/contacts/{{contactId}}` | [docs](https://wordpress.org/plugins/thrivedesk/) |
| [Update Conversation](actions/update-conversation.md) | `PATCH /v1/conversation/{{conversationId}}` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Update Conversation Priority](actions/update-conversation-priority.md) | `PUT /v1/conversation/{{conversationId}}/update/priority` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Update Inbox Automation](actions/update-inbox-automation.md) | `POST /v1/inboxes/{{inboxId}}/automations/{{automationId}}` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Update Inbox Permissions](actions/update-inbox-permissions.md) | `PATCH /v1/settings/inbox/{{inboxId}}/permissions` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Update Inbox Satisfaction Ratings](actions/update-inbox-satisfaction-ratings.md) | `PUT /v1/settings/inbox/{{inboxId}}/satisfaction-ratings` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Update Inbox Settings](actions/update-inbox-settings.md) | `PUT /v1/settings/inbox/{{inboxId}}` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Update Knowledge Base](actions/update-knowledge-base.md) | `POST /v1/knowledgebases/{{knowledgebaseId}}` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Update New Conversation](actions/update-new-conversation.md) | `POST /v1/conversation/{{conversationId}}/update-new-conversation` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Update Notification Preferences](actions/update-notification-preferences.md) | `POST /v1/notifications/preferences` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Update Saved Reply](actions/update-saved-reply.md) | `PUT /v1/saved-replies/{{savedReplyId}}` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Update Saved Reply Folder](actions/update-saved-reply-folder.md) | `PATCH /v1/saved-replies/folder` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Update Settings Tag](actions/update-settings-tag.md) | `PUT /v1/settings/tags/{{tagId}}` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Update Settings User](actions/update-settings-user.md) | `PUT /v1/settings/users/{{userId}}` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Update User Permissions](actions/update-user-permissions.md) | `POST /v1/settings/users/{{userId}}/permissions` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Update User Role](actions/update-user-role.md) | `PUT /v1/settings/users/{{userId}}/role` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Use Saved Reply](actions/use-saved-reply.md) | `POST /v1/saved-replies/{{savedReplyId}}/use` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Validate Inbox Alias](actions/validate-inbox-alias.md) | `POST /v1/settings/inbox/{{inboxId}}/aliases/validate` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Validate Inbox Connection](actions/validate-inbox-connection.md) | `POST /v1/settings/inbox/{{inboxId}}/connection/validate` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Validate Settings User](actions/validate-settings-user.md) | `POST /v1/settings/users/validate` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Verify Inbox Alias Code](actions/verify-inbox-alias-code.md) | `POST /v1/settings/inbox/{{inboxId}}/aliases/{{aliasId}}/verify-code` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
| [Verify Inbox Connection](actions/verify-inbox-connection.md) | `POST /v1/settings/inbox/{{inboxId}}/connection/verify` | [docs](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP) |
