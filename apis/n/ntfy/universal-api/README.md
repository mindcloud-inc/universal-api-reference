# <img src="https://images.mindcloud.co/apps/icons/ntfy_1776194972170.png" alt="ntfy logo" width="28" height="28"> ntfy: Universal API

Send and retrieve notifications, inspect topic metadata, and manage public ntfy topic workflows against the ntfy HTTP API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/ntfy/latest
- **Category:** Communication / Team Messaging
- **Actions:** 49
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://ntfy.sh
- **Vendor API docs:** https://docs.ntfy.sh/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Cached Topic Messages](actions/list-cached-topic-messages.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ntfy/latest/actions/list-cached-topic-messages?connectionId=$CONNECTION_ID&topic=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (49)

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Scheduled Notification](actions/cancel-scheduled-notification.md) | DELETE | Cancels a scheduled ntfy message by sequence ID. |
| [Clear Notification](actions/clear-notification.md) | DELETE | Clears an ntfy message by sequence ID. |
| [Clear Notification Read Alias](actions/clear-notification-read-alias.md) | DELETE | Marks an ntfy message as read by sequence ID. |
| [Delete Notification](actions/delete-notification.md) | DELETE | Deletes an ntfy message by sequence ID. |
| [List Cached Topic Messages](actions/list-cached-topic-messages.md) | GET | Retrieves cached messages from an ntfy topic. |
| [List Latest Topic Messages](actions/list-latest-topic-messages.md) | GET | Retrieves the latest message from an ntfy topic. |
| [List Scheduled Topic Messages](actions/list-scheduled-topic-messages.md) | GET | Retrieves scheduled messages from an ntfy topic. |
| [Publish Alertmanager Template Notification](actions/publish-alertmanager-template-notification.md) | POST | Publishes an ntfy notification from the Alertmanager template. |
| [Publish Attachment Upload](actions/publish-attachment-upload.md) | POST | Publishes a file attachment to an ntfy topic. |
| [Publish Broadcast Action Notification](actions/publish-broadcast-action-notification.md) | POST | Publishes an ntfy notification with a broadcast action. |
| [Publish Clickable Message](actions/publish-clickable-message.md) | POST | Publishes a message with a click URL in ntfy. |
| [Publish Copy Action Notification](actions/publish-copy-action-notification.md) | POST | Publishes an ntfy notification with a copy action. |
| [Publish Custom Template Notification](actions/publish-custom-template-notification.md) | POST | Publishes an ntfy notification from a custom template. |
| [Publish Email Notification](actions/publish-email-notification.md) | POST | Publishes an email notification in ntfy. |
| [Publish GitHub Template Notification](actions/publish-git-hub-template-notification.md) | POST | Publishes an ntfy notification from the GitHub template. |
| [Publish Grafana Template Notification](actions/publish-grafana-template-notification.md) | POST | Publishes an ntfy notification from the Grafana template. |
| [Publish HTTP Action Notification](actions/publish-http-action-notification.md) | POST | Publishes an ntfy notification with an HTTP action. |
| [Publish Inline Template Notification](actions/publish-inline-template-notification.md) | POST | Publishes an ntfy notification from an inline template. |
| [Publish JSON Message](actions/publish-json-message.md) | POST | Publishes a JSON message to an ntfy topic. |
| [Publish Markdown Message](actions/publish-markdown-message.md) | POST | Publishes a Markdown message to an ntfy topic. |
| [Publish Matrix Gateway Notification](actions/publish-matrix-gateway-notification.md) | POST | Publishes a Matrix gateway notification through ntfy. |
| [Publish Message](actions/publish-message.md) | POST | Publishes a message to an ntfy topic. |
| [Publish Message With Action Buttons](actions/publish-message-with-action-buttons.md) | POST | Publishes a message with action buttons in ntfy. |
| [Publish Message With Attachment URL](actions/publish-message-with-attachment-url.md) | POST | Publishes a message with an attachment URL in ntfy. |
| [Publish Message With Filename](actions/publish-message-with-filename.md) | POST | Publishes a message with an attachment filename in ntfy. |
| [Publish Message With Icon](actions/publish-message-with-icon.md) | POST | Publishes a message with an icon in ntfy. |
| [Publish Message With Title](actions/publish-message-with-title.md) | POST | Publishes a message to an ntfy topic with a title. |
| [Publish Notification With Sequence ID](actions/publish-notification-with-sequence-id.md) | POST | Publishes a message to an ntfy topic by sequence ID. |
| [Publish Phone Call](actions/publish-phone-call.md) | POST | Publishes a phone call notification in ntfy. |
| [Publish Predefined Template Notification](actions/publish-predefined-template-notification.md) | POST | Publishes an ntfy notification from a predefined template. |
| [Publish Priority Message](actions/publish-priority-message.md) | POST | Publishes a priority message to an ntfy topic. |
| [Publish Scheduled Message At](actions/publish-scheduled-message-at.md) | POST | Schedules a message in an ntfy topic at a specific time. |
| [Publish Scheduled Message In](actions/publish-scheduled-message-in.md) | POST | Schedules a message in an ntfy topic after a delay. |
| [Publish Tagged Message](actions/publish-tagged-message.md) | POST | Publishes a tagged message to an ntfy topic. |
| [Publish UnifiedPush Message](actions/publish-unified-push-message.md) | POST | Publishes a UnifiedPush message to an ntfy topic. |
| [Publish Via GET](actions/publish-via-get.md) | POST | Publishes a message to an ntfy topic via GET. |
| [Publish View Action Notification](actions/publish-view-action-notification.md) | POST | Publishes an ntfy notification with a view action. |
| [Publish Without Cache](actions/publish-without-cache.md) | POST | Publishes a message to ntfy without server-side caching. |
| [Publish Without Firebase](actions/publish-without-firebase.md) | POST | Publishes a message to ntfy without Firebase delivery. |
| [Send Webhook](actions/send-webhook.md) | POST | Sends a GET webhook message to an ntfy topic. |
| [Subscribe Multiple Topics JSON Stream](actions/subscribe-multiple-topics-json-stream.md) | GET | Subscribes to multiple ntfy topics as a JSON stream. |
| [Subscribe Multiple Topics Raw Stream](actions/subscribe-multiple-topics-raw-stream.md) | GET | Subscribes to multiple ntfy topics as a raw stream. |
| [Subscribe Multiple Topics SSE Stream](actions/subscribe-multiple-topics-sse-stream.md) | GET | Subscribes to multiple ntfy topics as an SSE stream. |
| [Subscribe Topic JSON Stream](actions/subscribe-topic-json-stream.md) | GET | Subscribes to an ntfy topic as a JSON stream. |
| [Subscribe Topic Raw Stream](actions/subscribe-topic-raw-stream.md) | GET | Subscribes to an ntfy topic as a raw stream. |
| [Subscribe Topic SSE Stream](actions/subscribe-topic-sse-stream.md) | GET | Subscribes to an ntfy topic as an SSE stream. |
| [Subscribe Topic WebSocket Stream](actions/subscribe-topic-web-socket-stream.md) | GET | Subscribes to an ntfy topic over WebSockets. |
| [Trigger Webhook](actions/trigger-webhook.md) | POST | Triggers an ntfy topic webhook via GET. |
| [Update Notification By Header Sequence ID](actions/update-notification-by-header-sequence-id.md) | PUT | Updates an ntfy message by sequence ID header. |

