# Next Cloud OCS: Native API Reference

A consolidated summary of Next Cloud OCS's API configuration and 383 documented operations, with links to official documentation.

- **Official docs:** https://docs.nextcloud.com/server/latest/developer_manual/client_apis/OCS/ocs-api-overview.html
- **API base URL:** `https://demo2.nextcloud.com`

## Authentication

### Basic auth

Use a Nextcloud username and password or app password. OCS requests require Basic auth and the OCS-APIRequest header.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://docs.nextcloud.com/server/latest/developer_manual/client_apis/OCS/ocs-api-overview.html)

## API conventions

Request bodies use URL-encoded form data.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/x-www-form-urlencoded` |

Responses from this API use JSON.

## Endpoints (383 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Accept Cloud Share](actions/accept-cloud-share.md) | `POST /ocs/v2.php/cloud/shares/{{id}}/accept` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Accept File Ownership Transfer](actions/accept-file-ownership-transfer.md) | `POST /ocs/v2.php/apps/files/api/v1/transferownership/{{id}}` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Accept Pending Remote Share](actions/accept-pending-remote-share.md) | `POST /ocs/v2.php/apps/files_sharing/api/v1/remote_shares/pending/{{shareId}}` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/client_apis/OCS/ocs-share-api.html#accept-a-pending-federated-cloud-share) |
| [Accept Pending Share](actions/accept-pending-share.md) | `POST /ocs/v2.php/apps/files_sharing/api/v1/shares/pending/{{id}}` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/client_apis/OCS/ocs-share-api.html) |
| [Activate Web Push Device](actions/activate-web-push-device.md) | `POST /ocs/v2.php/apps/notifications/api/v2/webpush/activate` | [docs](https://github.com/nextcloud/notifications/blob/master/openapi-full.json) |
| [Add Active Talk Participant](actions/add-active-talk-participant.md) | `POST /ocs/v2.php/apps/spreed/api/v4/room/{{token}}/participants/active` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/participant/) |
| [Add Resource To Collaboration Collection](actions/add-resource-to-collaboration-collection.md) | `POST /ocs/v2.php/collaboration/resources/collections/{{collectionId}}` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Add Talk Bot Reaction](actions/add-talk-bot-reaction.md) | `POST /ocs/v2.php/apps/spreed/api/v4/bot/{{token}}/reaction/{{messageId}}` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/bots/) |
| [Add Talk Message Reaction](actions/add-talk-message-reaction.md) | `POST /ocs/v2.php/apps/spreed/api/v4/reaction/{{token}}/{{messageId}}` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/reaction/) |
| [Add Talk Participant](actions/add-talk-participant.md) | `POST /ocs/v2.php/apps/spreed/api/v4/room/{{token}}/participants` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/participant/) |
| [Add User Subadmin](actions/add-user-subadmin.md) | `POST /ocs/v1.php/cloud/users/{{userId}}/subadmins` | [docs](https://docs.nextcloud.com/server/latest/admin_manual/configuration_user/instruction_set_for_users.html) |
| [Add User To Group](actions/add-user-to-group.md) | `POST /ocs/v1.php/cloud/users/{{userId}}/groups` | [docs](https://docs.nextcloud.com/server/latest/admin_manual/configuration_user/instruction_set_for_users.html#add-user-to-group) |
| [Allow Talk Guests](actions/allow-talk-guests.md) | `POST /ocs/v2.php/apps/spreed/api/v4/room/{{token}}/public` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/conversation/#allow-guests-in-a-conversation-public-conversation) |
| [Assign Talk Breakout Attendees](actions/assign-talk-breakout-attendees.md) | `POST /ocs/v2.php/apps/spreed/api/v4/breakout-rooms/{{token}}/attendees` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/breakout-rooms/) |
| [Authenticate Talk Public Share](actions/authenticate-talk-public-share.md) | `POST /ocs/v2.php/apps/spreed/api/v4/publicshareauth` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/integration/) |
| [Broadcast To Talk Breakout Rooms](actions/broadcast-to-talk-breakout-rooms.md) | `POST /ocs/v2.php/apps/spreed/api/v4/breakout-rooms/{{token}}/broadcast` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/breakout-rooms/) |
| [Cancel Consumer Task](actions/cancel-consumer-task.md) | `POST /ocs/v2.php/taskprocessing/tasks_consumer/tasks/{{taskId}}/cancel` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Cancel Talk Breakout Assistance](actions/cancel-talk-breakout-assistance.md) | `DELETE /ocs/v2.php/apps/spreed/api/v4/breakout-rooms/{{token}}/request-assistance` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/breakout-rooms/) |
| [Cancel Task Processing Task](actions/cancel-task-processing-task.md) | `POST /ocs/v2.php/taskprocessing/tasks/{{taskId}}/cancel` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Check Notifications Exist](actions/check-notifications-exist.md) | `POST /ocs/v2.php/apps/notifications/api/v2/notifications/exists` | [docs](https://github.com/nextcloud/notifications/blob/master/docs/ocs-endpoint-v2.md) |
| [Check Text To Image Availability](actions/check-text-to-image-availability.md) | `GET /ocs/v2.php/text2image/is_available` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Clear LDAP Wizard Mappings](actions/clear-ldap-wizard-mappings.md) | `POST /ocs/v2.php/apps/user_ldap/api/v1/wizard/clearMappings` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Clear Out Of Office](actions/clear-out-of-office.md) | `DELETE /ocs/v2.php/apps/dav/api/v1/outOfOffice/{{userId}}` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/client_apis/OCS/ocs-out-of-office-api.html#clear-data-and-disable-out-of-office) |
| [Clear Rejected Talk Dial Out](actions/clear-rejected-talk-dial-out.md) | `DELETE /ocs/v2.php/apps/spreed/api/v4/room/{{token}}/rejected-dialout` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/participant/) |
| [Clear Status Message](actions/clear-status-message.md) | `DELETE /ocs/v2.php/apps/user_status/api/v1/user_status/message` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/client_apis/OCS/ocs-status-api.html#clear-message) |
| [Clear Talk Chat History](actions/clear-talk-chat-history.md) | `DELETE /ocs/v2.php/apps/spreed/api/v4/chat/{{token}}` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/chat/) |
| [Configure Talk Breakout Rooms](actions/configure-talk-breakout-rooms.md) | `POST /ocs/v2.php/apps/spreed/api/v4/breakout-rooms/{{token}}` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/breakout-rooms/) |
| [Confirm App Password](actions/confirm-app-password.md) | `PUT /ocs/v2.php/core/apppassword/confirm` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Convert File](actions/convert-file.md) | `POST /ocs/v2.php/apps/files/api/v1/convert` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Copy LDAP Config](actions/copy-ldap-config.md) | `POST /ocs/v2.php/apps/user_ldap/api/v1/config/{{configID}}/copy` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Create Admin Notification](actions/create-admin-notification.md) | `POST /ocs/v2.php/apps/notifications/api/v2/admin_notifications/{{userId}}` | [docs](https://github.com/nextcloud/notifications/blob/master/docs/admin-notifications.md) |
| [Create Admin Notification V3](actions/create-admin-notification-v3.md) | `POST /ocs/v2.php/apps/notifications/api/v3/admin_notifications/{{userId}}` | [docs](https://github.com/nextcloud/notifications/blob/master/openapi-full.json) |
| [Create Cloud Group V2](actions/create-cloud-group-v2.md) | `POST /ocs/v2.php/cloud/groups` | [docs](https://docs.nextcloud.com/server/latest/admin_manual/configuration_user/instruction_set_for_groups.html) |
| [Create Cloud Share](actions/create-cloud-share.md) | `POST /ocs/v2.php/cloud/shares` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Create Cloud User V2](actions/create-cloud-user-v2.md) | `POST /ocs/v2.php/cloud/users` | [docs](https://docs.nextcloud.com/server/latest/admin_manual/configuration_user/instruction_set_for_users.html) |
| [Create Collaboration Resource](actions/create-collaboration-resource.md) | `POST /ocs/v2.php/collaboration/resources/{{baseResourceType}}/{{baseResourceId}}` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Create Direct Download Link](actions/create-direct-download-link.md) | `POST /ocs/v2.php/apps/dav/api/v1/direct` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/client_apis/OCS/ocs-api-overview.html#direct-download) |
| [Create Direct Editing File](actions/create-direct-editing-file.md) | `POST /ocs/v2.php/apps/files/api/v1/directEditing/create` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/client_apis/OCS/ocs-api-overview.html#capabilities-api) |
| [Create File From Template](actions/create-file-from-template.md) | `POST /ocs/v2.php/apps/files/api/v1/templates/create` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Create Global Workflow](actions/create-global-workflow.md) | `POST /ocs/v2.php/apps/workflowengine/api/v1/workflows/global` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Create Group](actions/create-group.md) | `POST /ocs/v1.php/cloud/groups` | [docs](https://docs.nextcloud.com/server/latest/admin_manual/configuration_user/instruction_set_for_groups.html#create-a-group) |
| [Create LDAP Config](actions/create-ldap-config.md) | `POST /ocs/v2.php/apps/user_ldap/api/v1/config` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Create Richdocuments Document Link](actions/create-richdocuments-document-link.md) | `POST /ocs/v2.php/apps/richdocuments/api/v1/document` | [docs](https://collabora-online-for-nextcloud.readthedocs.io/en/latest/mobile_editor/) |
| [Create Richdocuments Share Link](actions/create-richdocuments-share-link.md) | `POST /ocs/v2.php/apps/richdocuments/api/v1/share` | [docs](https://collabora-online-for-nextcloud.readthedocs.io/en/latest/mobile_editor/) |
| [Create Share](actions/create-share.md) | `POST /ocs/v2.php/apps/files_sharing/api/v1/shares` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/client_apis/OCS/ocs-share-api.html#create-a-new-share) |
| [Create Talk Conversation](actions/create-talk-conversation.md) | `POST /ocs/v2.php/apps/spreed/api/v4/room` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/conversation/#creating-a-new-conversation) |
| [Create Talk Message Reminder](actions/create-talk-message-reminder.md) | `POST /ocs/v2.php/apps/spreed/api/v4/chat/{{token}}/{{messageId}}/reminder` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/chat/) |
| [Create Talk Poll](actions/create-talk-poll.md) | `POST /ocs/v2.php/apps/spreed/api/v4/poll/{{token}}` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/poll/) |
| [Create Trusted Server](actions/create-trusted-server.md) | `POST /ocs/v2.php/apps/federation/trusted-servers` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Create User](actions/create-user.md) | `POST /ocs/v1.php/cloud/users` | [docs](https://docs.nextcloud.com/server/latest/admin_manual/configuration_user/instruction_set_for_users.html) |
| [Create User Workflow](actions/create-user-workflow.md) | `POST /ocs/v2.php/apps/workflowengine/api/v1/workflows/user` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Create Webhook](actions/create-webhook.md) | `POST /ocs/v2.php/apps/webhook_listeners/api/v1/webhooks` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Decline Cloud Share](actions/decline-cloud-share.md) | `POST /ocs/v2.php/cloud/shares/{{id}}/decline` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Decline Pending Remote Share](actions/decline-pending-remote-share.md) | `DELETE /ocs/v2.php/apps/files_sharing/api/v1/remote_shares/pending/{{shareId}}` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/client_apis/OCS/ocs-share-api.html#decline-a-pending-federated-cloud-share) |
| [Delete All Notifications](actions/delete-all-notifications.md) | `DELETE /ocs/v2.php/apps/notifications/api/v2/notifications` | [docs](https://github.com/nextcloud/notifications/blob/master/docs/ocs-endpoint-v2.md) |
| [Delete App Config Value](actions/delete-app-config-value.md) | `DELETE /ocs/v2.php/apps/provisioning_api/api/v1/config/apps/{{app}}/{{key}}` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Delete App Password](actions/delete-app-password.md) | `DELETE /ocs/v2.php/core/apppassword` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Delete App Webhooks](actions/delete-app-webhooks.md) | `DELETE /ocs/v2.php/apps/webhook_listeners/api/v1/webhooks/byappid/{{appid}}` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Delete Cloud Group V2](actions/delete-cloud-group-v2.md) | `DELETE /ocs/v2.php/cloud/groups/{{groupId}}` | [docs](https://docs.nextcloud.com/server/latest/admin_manual/configuration_user/instruction_set_for_groups.html) |
| [Delete Cloud User V2](actions/delete-cloud-user-v2.md) | `DELETE /ocs/v2.php/cloud/users/{{userId}}` | [docs](https://docs.nextcloud.com/server/latest/admin_manual/configuration_user/instruction_set_for_users.html) |
| [Delete Collaboration Collection](actions/delete-collaboration-collection.md) | `DELETE /ocs/v2.php/collaboration/resources/collections/{{collectionId}}` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Delete Consumer Task](actions/delete-consumer-task.md) | `DELETE /ocs/v2.php/taskprocessing/tasks_consumer/task/{{id}}` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Delete File Ownership Transfer](actions/delete-file-ownership-transfer.md) | `DELETE /ocs/v2.php/apps/files/api/v1/transferownership/{{id}}` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Delete File Reminder](actions/delete-file-reminder.md) | `DELETE /ocs/v2.php/apps/files_reminders/api/v{{version}}/{{fileId}}` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Delete Global Workflow](actions/delete-global-workflow.md) | `DELETE /ocs/v2.php/apps/workflowengine/api/v1/workflows/global/{{id}}` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Delete Group](actions/delete-group.md) | `DELETE /ocs/v1.php/cloud/groups/{{groupId}}` | [docs](https://docs.nextcloud.com/server/latest/admin_manual/configuration_user/instruction_set_for_groups.html#delete-a-group) |
| [Delete LDAP Config](actions/delete-ldap-config.md) | `DELETE /ocs/v2.php/apps/user_ldap/api/v1/config/{{configID}}` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Delete Notification](actions/delete-notification.md) | `DELETE /ocs/v2.php/apps/notifications/api/v2/notifications/{{notificationId}}` | [docs](https://github.com/nextcloud/notifications/blob/master/docs/ocs-endpoint-v1.md) |
| [Delete Remote Share](actions/delete-remote-share.md) | `DELETE /ocs/v2.php/apps/files_sharing/api/v1/remote_shares/{{shareId}}` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/client_apis/OCS/ocs-share-api.html#delete-an-accepted-federated-cloud-share) |
| [Delete Share](actions/delete-share.md) | `DELETE /ocs/v2.php/apps/files_sharing/api/v1/shares/{{shareId}}` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/client_apis/OCS/ocs-share-api.html#delete-share) |
| [Delete Talk Bot Reaction](actions/delete-talk-bot-reaction.md) | `DELETE /ocs/v2.php/apps/spreed/api/v4/bot/{{token}}/reaction/{{messageId}}` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/bots/) |
| [Delete Talk Chat Message](actions/delete-talk-chat-message.md) | `DELETE /ocs/v2.php/apps/spreed/api/v4/chat/{{token}}/{{messageId}}` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/chat/) |
| [Delete Talk Conversation](actions/delete-talk-conversation.md) | `DELETE /ocs/v2.php/apps/spreed/api/v4/room/{{token}}` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/conversation/#delete-a-conversation) |
| [Delete Talk Conversation Avatar](actions/delete-talk-conversation-avatar.md) | `DELETE /ocs/v2.php/apps/spreed/api/v4/room/{{token}}/avatar` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/avatar/) |
| [Delete Talk Message Reaction](actions/delete-talk-message-reaction.md) | `DELETE /ocs/v2.php/apps/spreed/api/v4/reaction/{{token}}/{{messageId}}` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/reaction/) |
| [Delete Talk Message Reminder](actions/delete-talk-message-reminder.md) | `DELETE /ocs/v2.php/apps/spreed/api/v4/chat/{{token}}/{{messageId}}/reminder` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/chat/) |
| [Delete Talk Poll](actions/delete-talk-poll.md) | `DELETE /ocs/v2.php/apps/spreed/api/v4/poll/{{token}}/{{pollId}}` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/poll/) |
| [Delete Talk Recording Notification](actions/delete-talk-recording-notification.md) | `DELETE /ocs/v2.php/apps/spreed/api/v4/recording/{{token}}/notification` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/recording/) |
| [Delete Task Processing Task](actions/delete-task-processing-task.md) | `DELETE /ocs/v2.php/taskprocessing/task/{{id}}` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Delete Text Processing Task](actions/delete-text-processing-task.md) | `DELETE /ocs/v2.php/textprocessing/task/{{id}}` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Delete Text To Image Task](actions/delete-text-to-image-task.md) | `DELETE /ocs/v2.php/text2image/task/{{id}}` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Delete Theming Theme](actions/delete-theming-theme.md) | `DELETE /ocs/v2.php/apps/theming/api/v1/theme/{{themeId}}` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Delete Trusted Server](actions/delete-trusted-server.md) | `DELETE /ocs/v2.php/apps/federation/trusted-servers/{{id}}` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Delete User](actions/delete-user.md) | `DELETE /ocs/v1.php/cloud/users/{{userId}}` | [docs](https://docs.nextcloud.com/server/latest/admin_manual/configuration_user/instruction_set_for_users.html) |
| [Delete User Preference](actions/delete-user-preference.md) | `DELETE /ocs/v2.php/apps/provisioning_api/api/v1/config/users/{{preferenceAppId}}/{{configKey}}` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/client_apis/OCS/ocs-user-preferences-api.html#deleting-a-preference) |
| [Delete User Preferences](actions/delete-user-preferences.md) | `DELETE /ocs/v2.php/apps/provisioning_api/api/v1/config/users/{{preferenceAppId}}` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/client_apis/OCS/ocs-user-preferences-api.html#deleting-multiple-preference) |
| [Delete User Workflow](actions/delete-user-workflow.md) | `DELETE /ocs/v2.php/apps/workflowengine/api/v1/workflows/user/{{id}}` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Delete Web Push Device](actions/delete-web-push-device.md) | `DELETE /ocs/v2.php/apps/notifications/api/v2/webpush` | [docs](https://github.com/nextcloud/notifications/blob/master/openapi-full.json) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /ocs/v2.php/apps/webhook_listeners/api/v1/webhooks/{{id}}` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Demote Talk Moderator](actions/demote-talk-moderator.md) | `DELETE /ocs/v2.php/apps/spreed/api/v4/room/{{token}}/moderators` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/participant/) |
| [Disable App](actions/disable-app.md) | `DELETE /ocs/v1.php/cloud/apps/{{appId}}` | [docs](https://docs.nextcloud.com/server/latest/admin_manual/configuration_user/instruction_set_for_apps.html) |
| [Disable Cloud App V2](actions/disable-cloud-app-v2.md) | `DELETE /ocs/v2.php/cloud/apps/{{app}}` | [docs](https://docs.nextcloud.com/server/latest/admin_manual/configuration_user/instruction_set_for_apps.html) |
| [Disable Cloud User V2](actions/disable-cloud-user-v2.md) | `PUT /ocs/v2.php/cloud/users/{{userId}}/disable` | [docs](https://docs.nextcloud.com/server/latest/admin_manual/configuration_user/instruction_set_for_users.html) |
| [Disable Talk Bot](actions/disable-talk-bot.md) | `DELETE /ocs/v2.php/apps/spreed/api/v4/bot/{{token}}/{{botId}}` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/bot-management/) |
| [Disable Two Factor Provider](actions/disable-two-factor-provider.md) | `POST /ocs/v2.php/twofactor/disable` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Disable User](actions/disable-user.md) | `PUT /ocs/v1.php/cloud/users/{{userId}}/disable` | [docs](https://docs.nextcloud.com/server/latest/admin_manual/configuration_user/instruction_set_for_users.html) |
| [Disallow Talk Guests](actions/disallow-talk-guests.md) | `DELETE /ocs/v2.php/apps/spreed/api/v4/room/{{token}}/public` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/conversation/#disallow-guests-in-a-conversation-group-conversation) |
| [Edit Talk Chat Message](actions/edit-talk-chat-message.md) | `PUT /ocs/v2.php/apps/spreed/api/v4/chat/{{token}}/{{messageId}}` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/chat/) |
| [Enable App](actions/enable-app.md) | `POST /ocs/v1.php/cloud/apps/{{appId}}` | [docs](https://docs.nextcloud.com/server/latest/admin_manual/configuration_user/instruction_set_for_apps.html) |
| [Enable Cloud App V2](actions/enable-cloud-app-v2.md) | `POST /ocs/v2.php/cloud/apps/{{app}}` | [docs](https://docs.nextcloud.com/server/latest/admin_manual/configuration_user/instruction_set_for_apps.html) |
| [Enable Cloud User V2](actions/enable-cloud-user-v2.md) | `PUT /ocs/v2.php/cloud/users/{{userId}}/enable` | [docs](https://docs.nextcloud.com/server/latest/admin_manual/configuration_user/instruction_set_for_users.html) |
| [Enable Talk Bot](actions/enable-talk-bot.md) | `POST /ocs/v2.php/apps/spreed/api/v4/bot/{{token}}/{{botId}}` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/bot-management/) |
| [Enable Theming Theme](actions/enable-theming-theme.md) | `PUT /ocs/v2.php/apps/theming/api/v1/theme/{{themeId}}/enable` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Enable Two Factor Provider](actions/enable-two-factor-provider.md) | `POST /ocs/v2.php/twofactor/enable` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Enable User](actions/enable-user.md) | `PUT /ocs/v1.php/cloud/users/{{userId}}/enable` | [docs](https://docs.nextcloud.com/server/latest/admin_manual/configuration_user/instruction_set_for_users.html) |
| [Extract Public References](actions/extract-public-references.md) | `POST /ocs/v2.php/references/extractPublic` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Extract References](actions/extract-references.md) | `POST /ocs/v2.php/references/extract` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Favorite Talk Conversation](actions/favorite-talk-conversation.md) | `POST /ocs/v2.php/apps/spreed/api/v4/room/{{token}}/favorite` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/conversation/#add-conversation-to-favorites) |
| [Get All Recommendations](actions/get-all-recommendations.md) | `GET /ocs/v2.php/apps/recommendations/api/v1/recommendations/always` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/client_apis/OCS/ocs-recommendations-api.html#fetch-user-setting-and-recommendations) |
| [Get App Config Value](actions/get-app-config-value.md) | `GET /ocs/v2.php/apps/provisioning_api/api/v1/config/apps/{{app}}/{{key}}` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Get App Info](actions/get-app-info.md) | `GET /ocs/v1.php/cloud/apps/{{appId}}` | [docs](https://docs.nextcloud.com/server/latest/admin_manual/configuration_user/instruction_set_for_apps.html#get-app-info) |
| [Get App Password](actions/get-app-password.md) | `GET /ocs/v2.php/core/getapppassword` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Get Backup User Status](actions/get-backup-user-status.md) | `GET /ocs/v2.php/apps/user_status/api/v1/statuses/_{{userId}}` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/client_apis/OCS/ocs-status-api.html#fetch-a-users-backup-status) |
| [Get Capabilities](actions/get-capabilities.md) | `GET /ocs/v1.php/cloud/capabilities` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/client_apis/OCS/ocs-api-overview.html#capabilities-api) |
| [Get Cloud App V2](actions/get-cloud-app-v2.md) | `GET /ocs/v2.php/cloud/apps/{{app}}` | [docs](https://docs.nextcloud.com/server/latest/admin_manual/configuration_user/instruction_set_for_apps.html) |
| [Get Cloud Capabilities V2](actions/get-cloud-capabilities-v2.md) | `GET /ocs/v2.php/cloud/capabilities` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Get Cloud Group V2](actions/get-cloud-group-v2.md) | `GET /ocs/v2.php/cloud/groups/{{groupId}}` | [docs](https://docs.nextcloud.com/server/latest/admin_manual/configuration_user/instruction_set_for_groups.html) |
| [Get Cloud Shared Secret](actions/get-cloud-shared-secret.md) | `GET /ocs/v2.php/cloud/shared-secret` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Get Cloud User V2](actions/get-cloud-user-v2.md) | `GET /ocs/v2.php/cloud/users/{{userId}}` | [docs](https://docs.nextcloud.com/server/latest/admin_manual/configuration_user/instruction_set_for_users.html) |
| [Get Collaboration Collection](actions/get-collaboration-collection.md) | `GET /ocs/v2.php/collaboration/resources/collections/{{collectionId}}` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Get Collaboration Resource](actions/get-collaboration-resource.md) | `GET /ocs/v2.php/collaboration/resources/{{resourceType}}/{{resourceId}}` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Get Consumer Task](actions/get-consumer-task.md) | `GET /ocs/v2.php/taskprocessing/tasks_consumer/task/{{id}}` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Get Current Cloud User V2](actions/get-current-cloud-user-v2.md) | `GET /ocs/v2.php/cloud/user` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Get Current Out Of Office](actions/get-current-out-of-office.md) | `GET /ocs/v2.php/apps/dav/api/v1/outOfOffice/{{userId}}/now` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/client_apis/OCS/ocs-out-of-office-api.html#fetch-ongoing-data) |
| [Get Current User](actions/get-current-user.md) | `GET /ocs/v1.php/cloud/user` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/client_apis/OCS/ocs-api-overview.html#user-metadata) |
| [Get Dark Talk Conversation Avatar](actions/get-dark-talk-conversation-avatar.md) | `GET /ocs/v2.php/apps/spreed/api/v4/room/{{token}}/avatar/dark` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/avatar/) |
| [Get Dark Talk Proxy User Avatar](actions/get-dark-talk-proxy-user-avatar.md) | `GET /ocs/v2.php/apps/spreed/api/v4/proxy/{{token}}/user-avatar/{{size}}/dark` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/avatar/) |
| [Get Dashboard Layout](actions/get-dashboard-layout.md) | `GET /ocs/v2.php/apps/dashboard/api/v3/layout` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Get Direct Editing Capabilities](actions/get-direct-editing-capabilities.md) | `GET /ocs/v2.php/apps/files/api/v1/directEditing` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/client_apis/OCS/ocs-api-overview.html#capabilities-api) |
| [Get Federation Shared Secret](actions/get-federation-shared-secret.md) | `GET /ocs/v2.php/apps/federation/api/v1/shared-secret` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Get File Reminder](actions/get-file-reminder.md) | `GET /ocs/v2.php/apps/files_reminders/api/v{{version}}/{{fileId}}` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Get File Template Fields](actions/get-file-template-fields.md) | `GET /ocs/v2.php/apps/files/api/v1/templates/fields/{{fileId}}` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Get Global Workflow](actions/get-global-workflow.md) | `GET /ocs/v2.php/apps/workflowengine/api/v1/workflows/global/{{id}}` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Get Group Members](actions/get-group-members.md) | `GET /ocs/v1.php/cloud/groups/{{groupId}}` | [docs](https://docs.nextcloud.com/server/latest/admin_manual/configuration_user/instruction_set_for_groups.html#get-members-of-a-group) |
| [Get Hovercard](actions/get-hovercard.md) | `GET /ocs/v2.php/hovercard/v1/{{userId}}` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Get Instance Status](actions/get-instance-status.md) | `GET /status.php` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Get LDAP Config](actions/get-ldap-config.md) | `GET /ocs/v2.php/apps/user_ldap/api/v1/config/{{configID}}` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Get Next Provider Task](actions/get-next-provider-task.md) | `GET /ocs/v2.php/taskprocessing/tasks_provider/next` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Get Next Provider Task Batch](actions/get-next-provider-task-batch.md) | `GET /ocs/v2.php/taskprocessing/tasks_provider/next_batch` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Get Notification](actions/get-notification.md) | `GET /ocs/v2.php/apps/notifications/api/v2/notifications/{{notificationId}}` | [docs](https://github.com/nextcloud/notifications/blob/master/docs/ocs-endpoint-v2.md) |
| [Get One Time App Password](actions/get-one-time-app-password.md) | `GET /ocs/v2.php/core/getapppassword-onetime` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Get Own Status](actions/get-own-status.md) | `GET /ocs/v2.php/apps/user_status/api/v1/user_status` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/client_apis/OCS/ocs-status-api.html#fetch-your-own-status) |
| [Get Profile](actions/get-profile.md) | `GET /ocs/v2.php/profile/{{targetUserId}}` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Get Provider Task File](actions/get-provider-task-file.md) | `GET /ocs/v2.php/taskprocessing/tasks_provider/{{taskId}}/file/{{fileId}}` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Get Recommendations](actions/get-recommendations.md) | `GET /ocs/v2.php/apps/recommendations/api/v1/recommendations` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/client_apis/OCS/ocs-recommendations-api.html#fetch-user-controlled-recommendations) |
| [Get Remote Share](actions/get-remote-share.md) | `GET /ocs/v2.php/apps/files_sharing/api/v1/remote_shares/{{shareId}}` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/client_apis/OCS/ocs-share-api.html#get-information-about-a-known-federated-cloud-share) |
| [Get Share](actions/get-share.md) | `GET /ocs/v2.php/apps/files_sharing/api/v1/shares/{{shareId}}` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/client_apis/OCS/ocs-share-api.html#get-information-about-a-known-share) |
| [Get Share Token](actions/get-share-token.md) | `GET /ocs/v2.php/apps/files_sharing/api/v1/token` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/client_apis/OCS/ocs-share-api.html) |
| [Get Shares For Path](actions/get-shares-for-path.md) | `GET /ocs/v2.php/apps/files_sharing/api/v1/shares` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/client_apis/OCS/ocs-share-api.html#get-shares-from-a-specific-file-or-folder) |
| [Get Talk Chat Message Context](actions/get-talk-chat-message-context.md) | `GET /ocs/v2.php/apps/spreed/api/v4/chat/{{token}}/{{messageId}}/context` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/chat/) |
| [Get Talk Conversation](actions/get-talk-conversation.md) | `GET /ocs/v2.php/apps/spreed/api/v4/room/{{token}}` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/conversation/#get-single-conversation-also-for-guests) |
| [Get Talk Conversation Avatar](actions/get-talk-conversation-avatar.md) | `GET /ocs/v2.php/apps/spreed/api/v4/room/{{token}}/avatar` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/avatar/) |
| [Get Talk Conversation Capabilities](actions/get-talk-conversation-capabilities.md) | `GET /ocs/v2.php/apps/spreed/api/v4/room/{{token}}/capabilities` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/conversation/#get-conversation-capabilities) |
| [Get Talk Dial In Participant](actions/get-talk-dial-in-participant.md) | `GET /ocs/v2.php/apps/spreed/api/v4/room/{{token}}/pin/{{pin}}` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/participant/) |
| [Get Talk File Integration](actions/get-talk-file-integration.md) | `GET /ocs/v2.php/apps/spreed/api/v4/file/{{fileId}}` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/integration/) |
| [Get Talk Message Reminder](actions/get-talk-message-reminder.md) | `GET /ocs/v2.php/apps/spreed/api/v4/chat/{{token}}/{{messageId}}/reminder` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/chat/) |
| [Get Talk Note To Self Conversation](actions/get-talk-note-to-self-conversation.md) | `GET /ocs/v2.php/apps/spreed/api/v4/room/note-to-self` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/conversation/#get-note-to-self-conversation) |
| [Get Talk Poll](actions/get-talk-poll.md) | `GET /ocs/v2.php/apps/spreed/api/v4/poll/{{token}}/{{pollId}}` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/poll/) |
| [Get Talk Proxy User Avatar](actions/get-talk-proxy-user-avatar.md) | `GET /ocs/v2.php/apps/spreed/api/v4/proxy/{{token}}/user-avatar/{{size}}` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/avatar/) |
| [Get Talk Public Share Integration](actions/get-talk-public-share-integration.md) | `GET /ocs/v2.php/apps/spreed/api/v4/publicshare/{{shareToken}}` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/integration/) |
| [Get Task Processing Queue Stats](actions/get-task-processing-queue-stats.md) | `GET /ocs/v2.php/taskprocessing/queue_stats` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Get Task Processing Task](actions/get-task-processing-task.md) | `GET /ocs/v2.php/taskprocessing/task/{{id}}` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Get Task Processing Task File](actions/get-task-processing-task-file.md) | `GET /ocs/v2.php/taskprocessing/tasks/{{taskId}}/file/{{fileId}}` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Get Team Resource](actions/get-team-resource.md) | `GET /ocs/v2.php/teams/resources/{{providerId}}/{{resourceId}}` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Get Templates Path](actions/get-templates-path.md) | `POST /ocs/v2.php/apps/files/api/v1/templates/path` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Get Text Processing Task](actions/get-text-processing-task.md) | `GET /ocs/v2.php/textprocessing/task/{{id}}` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Get Text To Image Result Image](actions/get-text-to-image-result-image.md) | `GET /ocs/v2.php/text2image/task/{{id}}/image/{{index}}` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Get Text To Image Task](actions/get-text-to-image-task.md) | `GET /ocs/v2.php/text2image/task/{{id}}` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Get Two Factor State](actions/get-two-factor-state.md) | `GET /ocs/v2.php/twofactor/state` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Get Upcoming Out Of Office](actions/get-upcoming-out-of-office.md) | `GET /ocs/v2.php/apps/dav/api/v1/outOfOffice/{{userId}}` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/client_apis/OCS/ocs-out-of-office-api.html#fetch-upcoming-or-ongoing-data) |
| [Get Update App Changelog](actions/get-update-app-changelog.md) | `GET /ocs/v2.php/apps/updatenotification/api/{{apiVersion}}/changelog/{{appId}}` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Get Update App List](actions/get-update-app-list.md) | `GET /ocs/v2.php/apps/updatenotification/api/{{apiVersion}}/applist/{{newVersion}}` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Get User Editable Fields](actions/get-user-editable-fields.md) | `GET /ocs/v2.php/cloud/user/fields/{{userId}}` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Get User Groups](actions/get-user-groups.md) | `GET /ocs/v1.php/cloud/users/{{userId}}/groups` | [docs](https://docs.nextcloud.com/server/latest/admin_manual/configuration_user/instruction_set_for_users.html#get-users-groups) |
| [Get User Groups Details](actions/get-user-groups-details.md) | `GET /ocs/v2.php/cloud/users/{{userId}}/groups/details` | [docs](https://docs.nextcloud.com/server/latest/admin_manual/configuration_user/instruction_set_for_users.html) |
| [Get User Metadata](actions/get-user-metadata.md) | `GET /ocs/v1.php/cloud/users/{{userId}}` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/client_apis/OCS/ocs-api-overview.html#user-metadata) |
| [Get User Status](actions/get-user-status.md) | `GET /ocs/v2.php/apps/user_status/api/v1/statuses/{{userId}}` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/client_apis/OCS/ocs-status-api.html#fetch-a-specific-users-status) |
| [Get User Subadmins Details](actions/get-user-subadmins-details.md) | `GET /ocs/v2.php/cloud/users/{{userId}}/subadmins/details` | [docs](https://docs.nextcloud.com/server/latest/admin_manual/configuration_user/instruction_set_for_users.html) |
| [Get User Workflow](actions/get-user-workflow.md) | `GET /ocs/v2.php/apps/workflowengine/api/v1/workflows/user/{{id}}` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Get Weather Forecast](actions/get-weather-forecast.md) | `GET /ocs/v2.php/apps/weather_status/api/v1/forecast` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Get Weather Location](actions/get-weather-location.md) | `GET /ocs/v2.php/apps/weather_status/api/v1/location` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/client_apis/OCS/ocs-api-overview.html#capabilities-api) |
| [Get Web Push Vapid Key](actions/get-web-push-vapid-key.md) | `GET /ocs/v2.php/apps/notifications/api/v2/webpush/vapid` | [docs](https://github.com/nextcloud/notifications/blob/master/openapi-full.json) |
| [Get Webhook](actions/get-webhook.md) | `GET /ocs/v2.php/apps/webhook_listeners/api/v1/webhooks/{{id}}` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Import Contacts File](actions/import-contacts-file.md) | `POST /ocs/v2.php/apps/contacts/api/v1/import/{{fileId}}` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/client_apis/ClientIntegration/index.html) |
| [Join Talk Call](actions/join-talk-call.md) | `POST /ocs/v2.php/apps/spreed/api/v4/call/{{token}}` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/call/) |
| [Leave Talk Call](actions/leave-talk-call.md) | `DELETE /ocs/v2.php/apps/spreed/api/v4/call/{{token}}` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/call/) |
| [Leave Talk Conversation](actions/leave-talk-conversation.md) | `DELETE /ocs/v2.php/apps/spreed/api/v4/room/{{token}}/participants/self` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/participant/) |
| [List Activity](actions/list-activity.md) | `GET /ocs/v2.php/apps/activity/api/v2/activity` | [docs](https://github.com/nextcloud/activity/blob/master/docs/endpoint-v2.md) |
| [List Activity By Filter](actions/list-activity-by-filter.md) | `GET /ocs/v2.php/apps/activity/api/v2/activity/{{filter}}` | [docs](https://github.com/nextcloud/activity/blob/master/docs/endpoint-v2.md) |
| [List Activity Filters](actions/list-activity-filters.md) | `GET /ocs/v2.php/apps/activity/api/v2/activity/filters` | [docs](https://github.com/nextcloud/activity/blob/master/docs/endpoint-v2.md) |
| [List App Config Apps](actions/list-app-config-apps.md) | `GET /ocs/v2.php/apps/provisioning_api/api/v1/config/apps` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [List App Config Keys](actions/list-app-config-keys.md) | `GET /ocs/v2.php/apps/provisioning_api/api/v1/config/apps/{{app}}` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [List Apps](actions/list-apps.md) | `GET /ocs/v1.php/cloud/apps` | [docs](https://docs.nextcloud.com/server/latest/admin_manual/configuration_user/instruction_set_for_apps.html#get-list-of-apps) |
| [List Cloud Apps V2](actions/list-cloud-apps-v2.md) | `GET /ocs/v2.php/cloud/apps` | [docs](https://docs.nextcloud.com/server/latest/admin_manual/configuration_user/instruction_set_for_apps.html) |
| [List Cloud Groups V2](actions/list-cloud-groups-v2.md) | `GET /ocs/v2.php/cloud/groups` | [docs](https://docs.nextcloud.com/server/latest/admin_manual/configuration_user/instruction_set_for_groups.html) |
| [List Cloud Users V2](actions/list-cloud-users-v2.md) | `GET /ocs/v2.php/cloud/users` | [docs](https://docs.nextcloud.com/server/latest/admin_manual/configuration_user/instruction_set_for_users.html) |
| [List Consumer Task Types](actions/list-consumer-task-types.md) | `GET /ocs/v2.php/taskprocessing/tasks_consumer/tasktypes` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [List Current User Apps](actions/list-current-user-apps.md) | `GET /ocs/v2.php/cloud/user/apps` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [List Dashboard Statuses](actions/list-dashboard-statuses.md) | `GET /ocs/v2.php/apps/dashboard/api/v3/statuses` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [List Dashboard Widget Items](actions/list-dashboard-widget-items.md) | `GET /ocs/v2.php/apps/dashboard/api/v1/widget-items` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [List Dashboard Widget Items V2](actions/list-dashboard-widget-items-v2.md) | `GET /ocs/v2.php/apps/dashboard/api/v2/widget-items` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [List Dashboard Widgets](actions/list-dashboard-widgets.md) | `GET /ocs/v2.php/apps/dashboard/api/v1/widgets` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [List Declarative Setting Forms](actions/list-declarative-setting-forms.md) | `GET /ocs/v2.php/settings/api/declarative/forms` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [List Deleted Shares](actions/list-deleted-shares.md) | `GET /ocs/v2.php/apps/files_sharing/api/v1/deletedshares` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/client_apis/OCS/ocs-share-api.html) |
| [List Direct Editing Templates](actions/list-direct-editing-templates.md) | `GET /ocs/v2.php/apps/files/api/v1/directEditing/templates/{{editorId}}/{{creatorId}}` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [List Disabled Users](actions/list-disabled-users.md) | `GET /ocs/v2.php/cloud/users/disabled` | [docs](https://docs.nextcloud.com/server/latest/admin_manual/configuration_user/instruction_set_for_users.html) |
| [List Editable User Fields](actions/list-editable-user-fields.md) | `GET /ocs/v1.php/cloud/user/fields` | [docs](https://docs.nextcloud.com/server/latest/admin_manual/configuration_user/instruction_set_for_users.html#list-of-editable-data-fields) |
| [List External Mounts](actions/list-external-mounts.md) | `GET /ocs/v2.php/apps/files_external/api/v1/mounts` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [List File Templates](actions/list-file-templates.md) | `GET /ocs/v2.php/apps/files/api/v1/templates` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [List Folder Tree](actions/list-folder-tree.md) | `GET /ocs/v2.php/apps/files/api/v1/folder-tree` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [List Global Workflows](actions/list-global-workflows.md) | `GET /ocs/v2.php/apps/workflowengine/api/v1/workflows/global` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [List Group Subadmins](actions/list-group-subadmins.md) | `GET /ocs/v2.php/cloud/groups/{{groupId}}/subadmins` | [docs](https://docs.nextcloud.com/server/latest/admin_manual/configuration_user/instruction_set_for_groups.html) |
| [List Group Users](actions/list-group-users.md) | `GET /ocs/v2.php/cloud/groups/{{groupId}}/users` | [docs](https://docs.nextcloud.com/server/latest/admin_manual/configuration_user/instruction_set_for_groups.html) |
| [List Group Users Details](actions/list-group-users-details.md) | `GET /ocs/v2.php/cloud/groups/{{groupId}}/users/details` | [docs](https://docs.nextcloud.com/server/latest/admin_manual/configuration_user/instruction_set_for_groups.html) |
| [List Groups](actions/list-groups.md) | `GET /ocs/v1.php/cloud/groups` | [docs](https://docs.nextcloud.com/server/latest/admin_manual/configuration_user/instruction_set_for_groups.html#search-get-groups) |
| [List Groups Details](actions/list-groups-details.md) | `GET /ocs/v2.php/cloud/groups/details` | [docs](https://docs.nextcloud.com/server/latest/admin_manual/configuration_user/instruction_set_for_groups.html) |
| [List Inherited Shares](actions/list-inherited-shares.md) | `GET /ocs/v2.php/apps/files_sharing/api/v1/shares/inherited` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/client_apis/OCS/ocs-status-api.html) |
| [List Navigation Apps](actions/list-navigation-apps.md) | `GET /ocs/v2.php/core/navigation/apps` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [List Navigation Settings](actions/list-navigation-settings.md) | `GET /ocs/v2.php/core/navigation/settings` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [List Notifications](actions/list-notifications.md) | `GET /ocs/v2.php/apps/notifications/api/v2/notifications` | [docs](https://github.com/nextcloud/notifications/blob/master/docs/ocs-endpoint-v1.md) |
| [List Open Talk Conversations](actions/list-open-talk-conversations.md) | `GET /ocs/v2.php/apps/spreed/api/v4/listed-room` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/conversation/#get-open-conversations) |
| [List Pending Remote Shares](actions/list-pending-remote-shares.md) | `GET /ocs/v2.php/apps/files_sharing/api/v1/remote_shares/pending` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/client_apis/OCS/ocs-share-api.html#list-pending-federated-cloud-shares) |
| [List Pending Shares](actions/list-pending-shares.md) | `GET /ocs/v2.php/apps/files_sharing/api/v1/shares/pending` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/client_apis/OCS/ocs-status-api.html) |
| [List Predefined Statuses](actions/list-predefined-statuses.md) | `GET /ocs/v2.php/apps/user_status/api/v1/predefined_statuses` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/client_apis/OCS/ocs-status-api.html#fetch-the-list-of-predefined-statuses) |
| [List Recent Users](actions/list-recent-users.md) | `GET /ocs/v2.php/cloud/users/recent` | [docs](https://docs.nextcloud.com/server/latest/admin_manual/configuration_user/instruction_set_for_users.html) |
| [List Reference Providers](actions/list-reference-providers.md) | `GET /ocs/v2.php/references/providers` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [List Remote Shares](actions/list-remote-shares.md) | `GET /ocs/v2.php/apps/files_sharing/api/v1/remote_shares` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/client_apis/OCS/ocs-share-api.html#list-accepted-federated-cloud-shares) |
| [List Search Providers](actions/list-search-providers.md) | `GET /ocs/v2.php/search/providers` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [List Sharee Recommendations](actions/list-sharee-recommendations.md) | `GET /ocs/v1.php/apps/files_sharing/api/v1/sharees_recommended` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/client_apis/OCS/ocs-sharee-api.html#sharee-recommendations) |
| [List Sharee Recommendations V2](actions/list-sharee-recommendations-v2.md) | `GET /ocs/v2.php/apps/files_sharing/api/v1/sharees_recommended` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [List Shares](actions/list-shares.md) | `GET /ocs/v2.php/apps/files_sharing/api/v1/shares` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/client_apis/OCS/ocs-share-api.html#get-all-shares) |
| [List Talk Bots](actions/list-talk-bots.md) | `GET /ocs/v2.php/apps/spreed/api/v4/bot/{{token}}` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/bot-management/) |
| [List Talk Bots Admin](actions/list-talk-bots-admin.md) | `GET /ocs/v2.php/apps/spreed/api/v4/bot/admin` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/bot-management/) |
| [List Talk Breakout Participants](actions/list-talk-breakout-participants.md) | `GET /ocs/v2.php/apps/spreed/api/v4/room/{{token}}/breakout-rooms/participants` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/participant/) |
| [List Talk Breakout Rooms](actions/list-talk-breakout-rooms.md) | `GET /ocs/v2.php/apps/spreed/api/v4/room/{{token}}/breakout-rooms` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/conversation/#get-breakout-rooms) |
| [List Talk Call Participants](actions/list-talk-call-participants.md) | `GET /ocs/v2.php/apps/spreed/api/v4/call/{{token}}` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/call/) |
| [List Talk Chat Messages](actions/list-talk-chat-messages.md) | `GET /ocs/v2.php/apps/spreed/api/v4/chat/{{token}}` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/chat/) |
| [List Talk Conversations](actions/list-talk-conversations.md) | `GET /ocs/v2.php/apps/spreed/api/v4/room` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/conversation/) |
| [List Talk Mentions](actions/list-talk-mentions.md) | `GET /ocs/v2.php/apps/spreed/api/v4/chat/{{token}}/mentions` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/chat/) |
| [List Talk Message Reactions](actions/list-talk-message-reactions.md) | `GET /ocs/v2.php/apps/spreed/api/v4/reaction/{{token}}/{{messageId}}` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/reaction/) |
| [List Talk Participants](actions/list-talk-participants.md) | `GET /ocs/v2.php/apps/spreed/api/v4/room/{{token}}/participants` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/participant/) |
| [List Talk Shared Items](actions/list-talk-shared-items.md) | `GET /ocs/v2.php/apps/spreed/api/v4/chat/{{token}}/share` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/chat/) |
| [List Talk Shared Items Overview](actions/list-talk-shared-items-overview.md) | `GET /ocs/v2.php/apps/spreed/api/v4/chat/{{token}}/share/overview` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/chat/) |
| [List Task Processing Task Types](actions/list-task-processing-task-types.md) | `GET /ocs/v2.php/taskprocessing/tasktypes` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [List Task Processing Tasks](actions/list-task-processing-tasks.md) | `GET /ocs/v2.php/taskprocessing/tasks` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [List Task Processing Tasks By App](actions/list-task-processing-tasks-by-app.md) | `GET /ocs/v2.php/taskprocessing/tasks/app/{{appId}}` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [List Team Resources](actions/list-team-resources.md) | `GET /ocs/v2.php/teams/{{teamId}}/resources` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [List Text Processing Task Types](actions/list-text-processing-task-types.md) | `GET /ocs/v2.php/textprocessing/tasktypes` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [List Text Processing Tasks By App](actions/list-text-processing-tasks-by-app.md) | `GET /ocs/v2.php/textprocessing/tasks/app/{{appId}}` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [List Text To Image Tasks By App](actions/list-text-to-image-tasks-by-app.md) | `GET /ocs/v2.php/text2image/tasks/app/{{appId}}` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [List Translation Languages](actions/list-translation-languages.md) | `GET /ocs/v2.php/translation/languages` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [List Trusted Servers](actions/list-trusted-servers.md) | `GET /ocs/v2.php/apps/federation/trusted-servers` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [List Upcoming Calendar Events](actions/list-upcoming-calendar-events.md) | `GET /ocs/v2.php/apps/dav/api/v1/events/upcoming` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [List User Statuses](actions/list-user-statuses.md) | `GET /ocs/v2.php/apps/user_status/api/v1/statuses` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/client_apis/OCS/ocs-status-api.html#fetch-a-list-of-all-set-user-statuses) |
| [List User Subadmins](actions/list-user-subadmins.md) | `GET /ocs/v1.php/cloud/users/{{userId}}/subadmins` | [docs](https://docs.nextcloud.com/server/latest/admin_manual/configuration_user/instruction_set_for_users.html) |
| [List User Workflows](actions/list-user-workflows.md) | `GET /ocs/v2.php/apps/workflowengine/api/v1/workflows/user` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [List Users](actions/list-users.md) | `GET /ocs/v1.php/cloud/users` | [docs](https://docs.nextcloud.com/server/latest/admin_manual/configuration_user/instruction_set_for_users.html#search-get-users) |
| [List Users Details](actions/list-users-details.md) | `GET /ocs/v2.php/cloud/users/details` | [docs](https://docs.nextcloud.com/server/latest/admin_manual/configuration_user/instruction_set_for_users.html) |
| [List Weather Favorites](actions/list-weather-favorites.md) | `GET /ocs/v2.php/apps/weather_status/api/v1/favorites` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [List Webhooks](actions/list-webhooks.md) | `GET /ocs/v2.php/apps/webhook_listeners/api/v1/webhooks` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Mark Talk Chat Read](actions/mark-talk-chat-read.md) | `POST /ocs/v2.php/apps/spreed/api/v4/chat/{{token}}/read` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/chat/) |
| [Mark Talk Chat Unread](actions/mark-talk-chat-unread.md) | `DELETE /ocs/v2.php/apps/spreed/api/v4/chat/{{token}}/read` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/chat/) |
| [Move Cloud Share](actions/move-cloud-share.md) | `POST /ocs/v2.php/cloud/shares/{{id}}/move` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Open Direct Editing File](actions/open-direct-editing-file.md) | `POST /ocs/v2.php/apps/files/api/v1/directEditing/open` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/client_apis/OCS/ocs-api-overview.html#capabilities-api) |
| [Open Local Editor](actions/open-local-editor.md) | `POST /ocs/v2.php/apps/files/api/v1/openlocaleditor` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Open Local Editor Token](actions/open-local-editor-token.md) | `POST /ocs/v2.php/apps/files/api/v1/openlocaleditor/{{token}}` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Promote Talk Moderator](actions/promote-talk-moderator.md) | `POST /ocs/v2.php/apps/spreed/api/v4/room/{{token}}/moderators` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/participant/) |
| [Register Push Device](actions/register-push-device.md) | `POST /ocs/v2.php/apps/notifications/api/v2/push` | [docs](https://github.com/nextcloud/notifications/blob/master/docs/push-v2.md) |
| [Register Talk Recording Backend](actions/register-talk-recording-backend.md) | `POST /ocs/v2.php/apps/spreed/api/v4/recording/backend` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/recording/) |
| [Register Web Push Device](actions/register-web-push-device.md) | `POST /ocs/v2.php/apps/notifications/api/v2/webpush` | [docs](https://github.com/nextcloud/notifications/blob/master/openapi-full.json) |
| [Remove Active Talk Participant](actions/remove-active-talk-participant.md) | `DELETE /ocs/v2.php/apps/spreed/api/v4/room/{{token}}/participants/active` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/participant/) |
| [Remove Talk Attendee](actions/remove-talk-attendee.md) | `DELETE /ocs/v2.php/apps/spreed/api/v4/room/{{token}}/attendees` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/participant/) |
| [Remove Talk Breakout Rooms](actions/remove-talk-breakout-rooms.md) | `DELETE /ocs/v2.php/apps/spreed/api/v4/breakout-rooms/{{token}}` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/breakout-rooms/) |
| [Remove User From Group](actions/remove-user-from-group.md) | `DELETE /ocs/v1.php/cloud/users/{{userId}}/groups` | [docs](https://docs.nextcloud.com/server/latest/admin_manual/configuration_user/instruction_set_for_users.html#remove-user-from-group) |
| [Remove User Subadmin](actions/remove-user-subadmin.md) | `DELETE /ocs/v1.php/cloud/users/{{userId}}/subadmins` | [docs](https://docs.nextcloud.com/server/latest/admin_manual/configuration_user/instruction_set_for_users.html) |
| [Rename Talk Conversation](actions/rename-talk-conversation.md) | `PUT /ocs/v2.php/apps/spreed/api/v4/room/{{token}}` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/conversation/#rename-a-conversation) |
| [Request Cloud Shared Secret](actions/request-cloud-shared-secret.md) | `POST /ocs/v2.php/cloud/shared-secret` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Request Federation Shared Secret](actions/request-federation-shared-secret.md) | `POST /ocs/v2.php/apps/federation/api/v1/request-shared-secret` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Request File Ownership Transfer](actions/request-file-ownership-transfer.md) | `POST /ocs/v2.php/apps/files/api/v1/transferownership` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Request Talk Breakout Assistance](actions/request-talk-breakout-assistance.md) | `POST /ocs/v2.php/apps/spreed/api/v4/breakout-rooms/{{token}}/request-assistance` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/breakout-rooms/) |
| [Resend Talk Invitations](actions/resend-talk-invitations.md) | `POST /ocs/v2.php/apps/spreed/api/v4/room/{{token}}/participants/resend-invitations` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/participant/) |
| [Resend User Welcome Email](actions/resend-user-welcome-email.md) | `POST /ocs/v1.php/cloud/users/{{userId}}/welcome` | [docs](https://docs.nextcloud.com/server/latest/admin_manual/configuration_user/instruction_set_for_users.html) |
| [Reshare Cloud Share](actions/reshare-cloud-share.md) | `POST /ocs/v2.php/cloud/shares/{{id}}/reshare` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Resolve Public Reference](actions/resolve-public-reference.md) | `GET /ocs/v2.php/references/resolvePublic` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Resolve Public Reference With Post](actions/resolve-public-reference-with-post.md) | `POST /ocs/v2.php/references/resolvePublic` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Resolve Reference](actions/resolve-reference.md) | `GET /ocs/v2.php/references/resolve` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Resolve Reference With Post](actions/resolve-reference-with-post.md) | `POST /ocs/v2.php/references/resolve` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Restore Backup Status](actions/restore-backup-status.md) | `DELETE /ocs/v2.php/apps/user_status/api/v1/statuses/revert/{{messageId}}` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/client_apis/OCS/ocs-status-api.html#user-status-restore-backup) |
| [Restore Deleted Share](actions/restore-deleted-share.md) | `POST /ocs/v2.php/apps/files_sharing/api/v1/deletedshares/{{id}}` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/client_apis/OCS/ocs-share-api.html) |
| [Restore User Status Message](actions/restore-user-status-message.md) | `DELETE /ocs/v2.php/apps/user_status/api/v1/user_status/revert/{{messageId}}` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/client_apis/OCS/ocs-status-api.html) |
| [Revoke Cloud Share](actions/revoke-cloud-share.md) | `POST /ocs/v2.php/cloud/shares/{{id}}/revoke` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Ring Talk Call Attendee](actions/ring-talk-call-attendee.md) | `POST /ocs/v2.php/apps/spreed/api/v4/call/{{token}}/ring/{{attendeeId}}` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/call/) |
| [Rotate App Password](actions/rotate-app-password.md) | `POST /ocs/v2.php/core/apppassword/rotate` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Run LDAP Wizard Action](actions/run-ldap-wizard-action.md) | `POST /ocs/v2.php/apps/user_ldap/api/v1/wizard/{{configID}}/{{wizardAction}}` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Schedule Consumer Task](actions/schedule-consumer-task.md) | `POST /ocs/v2.php/taskprocessing/tasks_consumer/schedule` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Schedule Task Processing Task](actions/schedule-task-processing-task.md) | `POST /ocs/v2.php/taskprocessing/schedule` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Schedule Text Processing Task](actions/schedule-text-processing-task.md) | `POST /ocs/v2.php/textprocessing/schedule` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Schedule Text To Image Task](actions/schedule-text-to-image-task.md) | `POST /ocs/v2.php/text2image/schedule` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Search Collaboration Collections](actions/search-collaboration-collections.md) | `GET /ocs/v2.php/collaboration/resources/collections/search/{{filter}}` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Search Core Autocomplete](actions/search-core-autocomplete.md) | `GET /ocs/v2.php/core/autocomplete/get` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/client_apis/OCS/ocs-api-overview.html#auto-complete-and-user-search) |
| [Search Provider](actions/search-provider.md) | `GET /ocs/v2.php/search/providers/{{providerId}}/search` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Search Sharees](actions/search-sharees.md) | `GET /ocs/v1.php/apps/files_sharing/api/v1/sharees` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/client_apis/OCS/ocs-sharee-api.html#search-sharees) |
| [Search Sharees V2](actions/search-sharees-v2.md) | `GET /ocs/v2.php/apps/files_sharing/api/v1/sharees` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Search Users By Phone](actions/search-users-by-phone.md) | `POST /ocs/v2.php/cloud/users/search/by-phone` | [docs](https://docs.nextcloud.com/server/latest/admin_manual/configuration_user/instruction_set_for_users.html) |
| [Send Share Email](actions/send-share-email.md) | `POST /ocs/v2.php/apps/files_sharing/api/v1/shares/{{shareId}}/send-email` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/client_apis/OCS/ocs-share-api.html#send-email) |
| [Send Talk Bot Message](actions/send-talk-bot-message.md) | `POST /ocs/v2.php/apps/spreed/api/v4/bot/{{token}}/message` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/bots/) |
| [Send Talk Chat Message](actions/send-talk-chat-message.md) | `POST /ocs/v2.php/apps/spreed/api/v4/chat/{{token}}` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/chat/) |
| [Send Test Notification To Self](actions/send-test-notification-to-self.md) | `POST /ocs/v2.php/apps/notifications/api/v3/test/self` | [docs](https://github.com/nextcloud/notifications/blob/master/openapi-full.json) |
| [Send User Status Heartbeat](actions/send-user-status-heartbeat.md) | `PUT /ocs/v2.php/apps/user_status/api/v1/heartbeat` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/client_apis/OCS/ocs-status-api.html) |
| [Set All Talk Attendee Permissions](actions/set-all-talk-attendee-permissions.md) | `PUT /ocs/v2.php/apps/spreed/api/v4/room/{{token}}/attendees/permissions/all` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/participant/) |
| [Set App Config Value](actions/set-app-config-value.md) | `POST /ocs/v2.php/apps/provisioning_api/api/v1/config/apps/{{app}}/{{key}}` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Set Cloud Share Permissions](actions/set-cloud-share-permissions.md) | `POST /ocs/v2.php/cloud/shares/{{id}}/permissions` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Set Custom Status Message](actions/set-custom-status-message.md) | `PUT /ocs/v2.php/apps/user_status/api/v1/user_status/message/custom` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/client_apis/OCS/ocs-status-api.html#set-a-custom-message-user-defined) |
| [Set Declarative Setting Value](actions/set-declarative-setting-value.md) | `POST /ocs/v2.php/settings/api/declarative/value` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Set File Reminder](actions/set-file-reminder.md) | `PUT /ocs/v2.php/apps/files_reminders/api/v{{version}}/{{fileId}}` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Set Own Status](actions/set-own-status.md) | `PUT /ocs/v2.php/apps/user_status/api/v1/user_status/status` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/client_apis/OCS/ocs-status-api.html#set-your-own-status) |
| [Set Predefined Status Message](actions/set-predefined-status-message.md) | `PUT /ocs/v2.php/apps/user_status/api/v1/user_status/message/predefined` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/client_apis/OCS/ocs-status-api.html#set-a-custom-message-predefined) |
| [Set Provider Task Result](actions/set-provider-task-result.md) | `POST /ocs/v2.php/taskprocessing/tasks_provider/{{taskId}}/result` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Set Reference Provider](actions/set-reference-provider.md) | `PUT /ocs/v2.php/references/provider/{{providerId}}` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Set Sensitive Declarative Setting Value](actions/set-sensitive-declarative-setting-value.md) | `POST /ocs/v2.php/settings/api/declarative/value-sensitive` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Set Talk Attendee Permissions](actions/set-talk-attendee-permissions.md) | `PUT /ocs/v2.php/apps/spreed/api/v4/room/{{token}}/attendees/permissions` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/participant/) |
| [Set Talk Call Notification Level](actions/set-talk-call-notification-level.md) | `POST /ocs/v2.php/apps/spreed/api/v4/room/{{token}}/notify-calls` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/conversation/#set-notification-level-for-calls) |
| [Set Talk Conversation Description](actions/set-talk-conversation-description.md) | `PUT /ocs/v2.php/apps/spreed/api/v4/room/{{token}}/description` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/conversation/#set-description-for-a-conversation) |
| [Set Talk Conversation Emoji Avatar](actions/set-talk-conversation-emoji-avatar.md) | `POST /ocs/v2.php/apps/spreed/api/v4/room/{{token}}/avatar/emoji` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/avatar/) |
| [Set Talk Guest Name](actions/set-talk-guest-name.md) | `POST /ocs/v2.php/apps/spreed/api/v4/guest/{{token}}/name` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/participant/) |
| [Set Talk Listable Scope](actions/set-talk-listable-scope.md) | `PUT /ocs/v2.php/apps/spreed/api/v4/room/{{token}}/listable` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/conversation/#open-a-conversation) |
| [Set Talk Mention Permissions](actions/set-talk-mention-permissions.md) | `PUT /ocs/v2.php/apps/spreed/api/v4/room/{{token}}/mention-permissions` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/conversation/#set-mention-permissions) |
| [Set Talk Message Expiration](actions/set-talk-message-expiration.md) | `POST /ocs/v2.php/apps/spreed/api/v4/room/{{token}}/message-expiration` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/conversation/#set-message-expiration) |
| [Set Talk Notification Level](actions/set-talk-notification-level.md) | `POST /ocs/v2.php/apps/spreed/api/v4/room/{{token}}/notify` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/conversation/#set-notification-level) |
| [Set Talk Participant State](actions/set-talk-participant-state.md) | `PUT /ocs/v2.php/apps/spreed/api/v4/room/{{token}}/participants/state` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/participant/) |
| [Set Talk Password](actions/set-talk-password.md) | `PUT /ocs/v2.php/apps/spreed/api/v4/room/{{token}}/password` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/conversation/#set-password-for-a-conversation) |
| [Set Talk Permissions](actions/set-talk-permissions.md) | `PUT /ocs/v2.php/apps/spreed/api/v4/room/{{token}}/permissions/{{mode}}` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/conversation/#set-default-or-call-permissions-for-a-conversation) |
| [Set Talk Read Only](actions/set-talk-read-only.md) | `PUT /ocs/v2.php/apps/spreed/api/v4/room/{{token}}/read-only` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/conversation/#set-read-only-for-a-conversation) |
| [Set Talk Recording Consent](actions/set-talk-recording-consent.md) | `PUT /ocs/v2.php/apps/spreed/api/v4/room/{{token}}/recording-consent` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/conversation/#set-recording-consent) |
| [Set Talk Webinar Lobby](actions/set-talk-webinar-lobby.md) | `PUT /ocs/v2.php/apps/spreed/api/v4/room/{{token}}/webinar/lobby` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/webinar/) |
| [Set Talk Webinar Sip](actions/set-talk-webinar-sip.md) | `PUT /ocs/v2.php/apps/spreed/api/v4/room/{{token}}/webinar/sip` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/webinar/) |
| [Set User Preference](actions/set-user-preference.md) | `POST /ocs/v2.php/apps/provisioning_api/api/v1/config/users/{{preferenceAppId}}/{{configKey}}` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/client_apis/OCS/ocs-user-preferences-api.html#setting-a-preference) |
| [Set User Preferences](actions/set-user-preferences.md) | `POST /ocs/v2.php/apps/provisioning_api/api/v1/config/users/{{preferenceAppId}}` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/client_apis/OCS/ocs-user-preferences-api.html#setting-multiple-preference) |
| [Share File To Talk Chat](actions/share-file-to-talk-chat.md) | `POST /ocs/v2.php/apps/spreed/api/v4/chat/{{token}}/share` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/chat/) |
| [Share Talk Recording To Chat](actions/share-talk-recording-to-chat.md) | `POST /ocs/v2.php/apps/spreed/api/v4/recording/{{token}}/share-chat` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/recording/) |
| [Start Talk Breakout Rooms](actions/start-talk-breakout-rooms.md) | `POST /ocs/v2.php/apps/spreed/api/v4/breakout-rooms/{{token}}/rooms` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/breakout-rooms/) |
| [Start Talk Dial Out](actions/start-talk-dial-out.md) | `POST /ocs/v2.php/apps/spreed/api/v4/call/{{token}}/dialout/{{attendeeId}}` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/call/) |
| [Start Talk Recording](actions/start-talk-recording.md) | `POST /ocs/v2.php/apps/spreed/api/v4/recording/{{token}}` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/recording/) |
| [Stop Talk Breakout Rooms](actions/stop-talk-breakout-rooms.md) | `DELETE /ocs/v2.php/apps/spreed/api/v4/breakout-rooms/{{token}}/rooms` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/breakout-rooms/) |
| [Stop Talk Recording](actions/stop-talk-recording.md) | `DELETE /ocs/v2.php/apps/spreed/api/v4/recording/{{token}}` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/recording/) |
| [Store Talk Recording](actions/store-talk-recording.md) | `POST /ocs/v2.php/apps/spreed/api/v4/recording/{{token}}/store` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/recording/) |
| [Switch Talk Breakout Room](actions/switch-talk-breakout-room.md) | `POST /ocs/v2.php/apps/spreed/api/v4/breakout-rooms/{{token}}/switch` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/breakout-rooms/) |
| [Test LDAP Config](actions/test-ldap-config.md) | `POST /ocs/v2.php/apps/user_ldap/api/v1/config/{{configID}}/test` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Translate Text](actions/translate-text.md) | `POST /ocs/v2.php/translation/translate` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Unfavorite Talk Conversation](actions/unfavorite-talk-conversation.md) | `DELETE /ocs/v2.php/apps/spreed/api/v4/room/{{token}}/favorite` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/conversation/#remove-conversation-from-favorites) |
| [Unregister Push Device](actions/unregister-push-device.md) | `DELETE /ocs/v2.php/apps/notifications/api/v2/push` | [docs](https://github.com/nextcloud/notifications/blob/master/docs/push-v2.md) |
| [Unshare Cloud Share](actions/unshare-cloud-share.md) | `POST /ocs/v2.php/cloud/shares/{{id}}/unshare` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Update Admin Notification Settings](actions/update-admin-notification-settings.md) | `POST /ocs/v2.php/apps/notifications/api/v2/settings/admin` | [docs](https://github.com/nextcloud/notifications/blob/master/openapi-full.json) |
| [Update Cloud User V2](actions/update-cloud-user-v2.md) | `PUT /ocs/v2.php/cloud/users/{{userId}}` | [docs](https://docs.nextcloud.com/server/latest/admin_manual/configuration_user/instruction_set_for_users.html) |
| [Update Collaboration Collection](actions/update-collaboration-collection.md) | `PUT /ocs/v2.php/collaboration/resources/collections/{{collectionId}}` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Update Dashboard Layout](actions/update-dashboard-layout.md) | `POST /ocs/v2.php/apps/dashboard/api/v3/layout` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Update Dashboard Statuses](actions/update-dashboard-statuses.md) | `POST /ocs/v2.php/apps/dashboard/api/v3/statuses` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Update Global Workflow](actions/update-global-workflow.md) | `PUT /ocs/v2.php/apps/workflowengine/api/v1/workflows/global/{{id}}` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Update Group](actions/update-group.md) | `PUT /ocs/v2.php/cloud/groups/{{groupId}}` | [docs](https://docs.nextcloud.com/server/latest/admin_manual/configuration_user/instruction_set_for_groups.html) |
| [Update LDAP Config](actions/update-ldap-config.md) | `PUT /ocs/v2.php/apps/user_ldap/api/v1/config/{{configID}}` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Update Notification Settings](actions/update-notification-settings.md) | `POST /ocs/v2.php/apps/notifications/api/v2/settings` | [docs](https://github.com/nextcloud/notifications/blob/master/openapi-full.json) |
| [Update Out Of Office](actions/update-out-of-office.md) | `POST /ocs/v2.php/apps/dav/api/v1/outOfOffice/{{userId}}` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/client_apis/OCS/ocs-out-of-office-api.html#modify-out-of-office-data) |
| [Update Profile](actions/update-profile.md) | `PUT /ocs/v2.php/profile/{{targetUserId}}` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Update Provider Task Progress](actions/update-provider-task-progress.md) | `POST /ocs/v2.php/taskprocessing/tasks_provider/{{taskId}}/progress` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Update Share](actions/update-share.md) | `PUT /ocs/v2.php/apps/files_sharing/api/v1/shares/{{shareId}}` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/client_apis/OCS/ocs-share-api.html#update-share) |
| [Update Talk Call Flags](actions/update-talk-call-flags.md) | `PUT /ocs/v2.php/apps/spreed/api/v4/call/{{token}}` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/call/) |
| [Update Talk Draft Poll](actions/update-talk-draft-poll.md) | `POST /ocs/v2.php/apps/spreed/api/v4/poll/{{token}}/draft/{{pollId}}` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/poll/) |
| [Update Talk Sip Settings](actions/update-talk-sip-settings.md) | `POST /ocs/v2.php/apps/spreed/api/v4/settings/sip` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/settings/) |
| [Update Talk User Settings](actions/update-talk-user-settings.md) | `POST /ocs/v2.php/apps/spreed/api/v4/settings/user` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/settings/) |
| [Update User Collection](actions/update-user-collection.md) | `PUT /ocs/v2.php/cloud/users/{{userId}}/{{collectionName}}` | [docs](https://docs.nextcloud.com/server/latest/admin_manual/configuration_user/instruction_set_for_users.html) |
| [Update User Field](actions/update-user-field.md) | `PUT /ocs/v1.php/cloud/users/{{userId}}` | [docs](https://docs.nextcloud.com/server/latest/admin_manual/configuration_user/instruction_set_for_users.html#edit-data-of-a-single-user) |
| [Update User Workflow](actions/update-user-workflow.md) | `PUT /ocs/v2.php/apps/workflowengine/api/v1/workflows/user/{{id}}` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Update Weather Favorites](actions/update-weather-favorites.md) | `PUT /ocs/v2.php/apps/weather_status/api/v1/favorites` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Update Weather Location](actions/update-weather-location.md) | `PUT /ocs/v2.php/apps/weather_status/api/v1/location` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Update Weather Mode](actions/update-weather-mode.md) | `PUT /ocs/v2.php/apps/weather_status/api/v1/mode` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Update Weather Personal Data Use](actions/update-weather-personal-data-use.md) | `PUT /ocs/v2.php/apps/weather_status/api/v1/use-personal` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Update Webhook](actions/update-webhook.md) | `POST /ocs/v2.php/apps/webhook_listeners/api/v1/webhooks/{{id}}` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Upload Provider Task File](actions/upload-provider-task-file.md) | `POST /ocs/v2.php/taskprocessing/tasks_provider/{{taskId}}/file` | [docs](https://docs.nextcloud.com/server/latest/developer_manual/_static/openapi.html) |
| [Upload Talk Conversation Avatar](actions/upload-talk-conversation-avatar.md) | `POST /ocs/v2.php/apps/spreed/api/v4/room/{{token}}/avatar` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/avatar/) |
| [Verify Talk Dial In](actions/verify-talk-dial-in.md) | `POST /ocs/v2.php/apps/spreed/api/v4/room/{{token}}/verify-dialin` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/participant/) |
| [Verify Talk Dial Out](actions/verify-talk-dial-out.md) | `POST /ocs/v2.php/apps/spreed/api/v4/room/{{token}}/verify-dialout` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/participant/) |
| [Vote Talk Poll](actions/vote-talk-poll.md) | `POST /ocs/v2.php/apps/spreed/api/v4/poll/{{token}}/{{pollId}}` | [docs](https://nextcloud-talk.readthedocs.io/en/stable/poll/) |
| [Wipe User Devices](actions/wipe-user-devices.md) | `POST /ocs/v2.php/cloud/users/{{userId}}/wipe` | [docs](https://docs.nextcloud.com/server/latest/admin_manual/configuration_user/instruction_set_for_users.html) |
