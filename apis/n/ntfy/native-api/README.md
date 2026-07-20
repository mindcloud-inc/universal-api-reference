# ntfy: Native API Reference

A consolidated summary of ntfy's API configuration and 49 documented operations, with links to official documentation.

- **Official docs:** https://docs.ntfy.sh/
- **API base URL:** `https://ntfy.sh`

## Authentication

### No Authentication

Use ntfy's public topic endpoints without credentials.

This API does not require request authentication.

[Official authentication documentation](https://docs.ntfy.sh/publish/#authentication)

## API conventions

Responses from this API use plain text.

## Endpoints (49 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Scheduled Notification](actions/cancel-scheduled-notification.md) | `DELETE /:topic/:sequence_id` | [docs](https://docs.ntfy.sh/publish/) |
| [Clear Notification](actions/clear-notification.md) | `PUT /:topic/:sequence_id/clear` | [docs](https://docs.ntfy.sh/publish/) |
| [Clear Notification Read Alias](actions/clear-notification-read-alias.md) | `PUT /:topic/:sequence_id/read` | [docs](https://docs.ntfy.sh/publish/) |
| [Delete Notification](actions/delete-notification.md) | `DELETE /:topic/:sequence_id` | [docs](https://docs.ntfy.sh/publish/) |
| [List Cached Topic Messages](actions/list-cached-topic-messages.md) | `GET /:topic/json` | [docs](https://docs.ntfy.sh/subscribe/api/#fetch-cached-messages) |
| [List Latest Topic Messages](actions/list-latest-topic-messages.md) | `GET /:topic/json` | [docs](https://docs.ntfy.sh/subscribe/api/) |
| [List Scheduled Topic Messages](actions/list-scheduled-topic-messages.md) | `GET /:topic/json` | [docs](https://docs.ntfy.sh/subscribe/api/) |
| [Publish Alertmanager Template Notification](actions/publish-alertmanager-template-notification.md) | `POST /:topic` | [docs](https://docs.ntfy.sh/publish/#pre-defined-templates) |
| [Publish Attachment Upload](actions/publish-attachment-upload.md) | `PUT /:topic` | [docs](https://docs.ntfy.sh/publish/) |
| [Publish Broadcast Action Notification](actions/publish-broadcast-action-notification.md) | `POST /:topic` | [docs](https://docs.ntfy.sh/publish/#send-android-broadcast) |
| [Publish Clickable Message](actions/publish-clickable-message.md) | `POST /:topic` | [docs](https://docs.ntfy.sh/publish/#click-action) |
| [Publish Copy Action Notification](actions/publish-copy-action-notification.md) | `POST /:topic` | [docs](https://docs.ntfy.sh/publish/#copy-to-clipboard) |
| [Publish Custom Template Notification](actions/publish-custom-template-notification.md) | `POST /:topic` | [docs](https://docs.ntfy.sh/publish/#custom-templates) |
| [Publish Email Notification](actions/publish-email-notification.md) | `POST /:topic` | [docs](https://docs.ntfy.sh/publish/#e-mail-notifications) |
| [Publish GitHub Template Notification](actions/publish-git-hub-template-notification.md) | `POST /:topic` | [docs](https://docs.ntfy.sh/publish/#pre-defined-templates) |
| [Publish Grafana Template Notification](actions/publish-grafana-template-notification.md) | `POST /:topic` | [docs](https://docs.ntfy.sh/publish/#pre-defined-templates) |
| [Publish HTTP Action Notification](actions/publish-http-action-notification.md) | `POST /:topic` | [docs](https://docs.ntfy.sh/publish/#send-http-request) |
| [Publish Inline Template Notification](actions/publish-inline-template-notification.md) | `POST /:topic` | [docs](https://docs.ntfy.sh/publish/#inline-templating) |
| [Publish JSON Message](actions/publish-json-message.md) | `POST /` | [docs](https://docs.ntfy.sh/publish/#publish-as-json) |
| [Publish Markdown Message](actions/publish-markdown-message.md) | `POST /:topic` | [docs](https://docs.ntfy.sh/publish/#markdown-formatting) |
| [Publish Matrix Gateway Notification](actions/publish-matrix-gateway-notification.md) | `POST /_matrix/push/v1/notify` | [docs](https://docs.ntfy.sh/publish/) |
| [Publish Message](actions/publish-message.md) | `POST /:topic` | [docs](https://docs.ntfy.sh/publish/) |
| [Publish Message With Action Buttons](actions/publish-message-with-action-buttons.md) | `POST /:topic` | [docs](https://docs.ntfy.sh/publish/#action-buttons) |
| [Publish Message With Attachment URL](actions/publish-message-with-attachment-url.md) | `POST /:topic` | [docs](https://docs.ntfy.sh/publish/#attach-file-from-a-url) |
| [Publish Message With Filename](actions/publish-message-with-filename.md) | `POST /:topic` | [docs](https://docs.ntfy.sh/publish/) |
| [Publish Message With Icon](actions/publish-message-with-icon.md) | `POST /:topic` | [docs](https://docs.ntfy.sh/publish/#icons) |
| [Publish Message With Title](actions/publish-message-with-title.md) | `POST /:topic` | [docs](https://docs.ntfy.sh/publish/#message-title) |
| [Publish Notification With Sequence ID](actions/publish-notification-with-sequence-id.md) | `POST /:topic/:sequence_id` | [docs](https://docs.ntfy.sh/publish/) |
| [Publish Phone Call](actions/publish-phone-call.md) | `POST /:topic` | [docs](https://docs.ntfy.sh/publish/#phone-calls) |
| [Publish Predefined Template Notification](actions/publish-predefined-template-notification.md) | `POST /:topic` | [docs](https://docs.ntfy.sh/publish/#pre-defined-templates) |
| [Publish Priority Message](actions/publish-priority-message.md) | `POST /:topic` | [docs](https://docs.ntfy.sh/publish/#message-priority) |
| [Publish Scheduled Message At](actions/publish-scheduled-message-at.md) | `POST /:topic` | [docs](https://docs.ntfy.sh/publish/) |
| [Publish Scheduled Message In](actions/publish-scheduled-message-in.md) | `POST /:topic` | [docs](https://docs.ntfy.sh/publish/) |
| [Publish Tagged Message](actions/publish-tagged-message.md) | `POST /:topic` | [docs](https://docs.ntfy.sh/publish/#tags-emojis) |
| [Publish UnifiedPush Message](actions/publish-unified-push-message.md) | `POST /:topic` | [docs](https://docs.ntfy.sh/publish/) |
| [Publish Via GET](actions/publish-via-get.md) | `GET /:topic/publish` | [docs](https://docs.ntfy.sh/publish/) |
| [Publish View Action Notification](actions/publish-view-action-notification.md) | `POST /:topic` | [docs](https://docs.ntfy.sh/publish/#open-websiteapp) |
| [Publish Without Cache](actions/publish-without-cache.md) | `POST /:topic` | [docs](https://docs.ntfy.sh/publish/) |
| [Publish Without Firebase](actions/publish-without-firebase.md) | `POST /:topic` | [docs](https://docs.ntfy.sh/publish/) |
| [Send Webhook](actions/send-webhook.md) | `GET /:topic/send` | [docs](https://docs.ntfy.sh/publish/) |
| [Subscribe Multiple Topics JSON Stream](actions/subscribe-multiple-topics-json-stream.md) | `GET /:topics/json` | [docs](https://docs.ntfy.sh/subscribe/api/#subscribe-to-multiple-topics) |
| [Subscribe Multiple Topics Raw Stream](actions/subscribe-multiple-topics-raw-stream.md) | `GET /:topics/raw` | [docs](https://docs.ntfy.sh/subscribe/api/#subscribe-to-multiple-topics) |
| [Subscribe Multiple Topics SSE Stream](actions/subscribe-multiple-topics-sse-stream.md) | `GET /:topics/sse` | [docs](https://docs.ntfy.sh/subscribe/api/#subscribe-to-multiple-topics) |
| [Subscribe Topic JSON Stream](actions/subscribe-topic-json-stream.md) | `GET /:topic/json` | [docs](https://docs.ntfy.sh/subscribe/api/#subscribe-as-json-stream) |
| [Subscribe Topic Raw Stream](actions/subscribe-topic-raw-stream.md) | `GET /:topic/raw` | [docs](https://docs.ntfy.sh/subscribe/api/#subscribe-as-raw-stream) |
| [Subscribe Topic SSE Stream](actions/subscribe-topic-sse-stream.md) | `GET /:topic/sse` | [docs](https://docs.ntfy.sh/subscribe/api/#subscribe-as-sse-stream) |
| [Subscribe Topic WebSocket Stream](actions/subscribe-topic-web-socket-stream.md) | `GET /:topic/ws` | [docs](https://docs.ntfy.sh/subscribe/api/#websockets) |
| [Trigger Webhook](actions/trigger-webhook.md) | `GET /:topic/trigger` | [docs](https://docs.ntfy.sh/publish/) |
| [Update Notification By Header Sequence ID](actions/update-notification-by-header-sequence-id.md) | `POST /:topic` | [docs](https://docs.ntfy.sh/publish/) |
