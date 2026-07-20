# Dify: Native API Reference

A consolidated summary of Dify's API configuration and 28 documented operations, with links to official documentation.

- **Official docs:** https://docs.dify.ai/api-reference
- **API base URL:** `https://api.dify.ai/v1`

## Authentication

### API Key

Use a Dify application API key in the Authorization bearer header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.dify.ai/en/use-dify/publish/developing-with-apis)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `limit` in the query string to set the page size (default 20; minimum 1).

## Endpoints (28 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Configure Annotation Reply](actions/configure-annotation-reply.md) | `POST /apps/annotation-reply/:action` | [docs](https://docs.dify.ai/api-reference/annotations/configure-annotation-reply) |
| [Convert Audio to Text](actions/convert-audio-to-text.md) | `POST /audio-to-text` | [docs](https://docs.dify.ai/api-reference/tts/convert-audio-to-text) |
| [Convert Text to Audio](actions/convert-text-to-audio.md) | `POST /text-to-audio` | [docs](https://docs.dify.ai/api-reference/tts/convert-text-to-audio) |
| [Create Annotation](actions/create-annotation.md) | `POST /apps/annotations` | [docs](https://docs.dify.ai/api-reference/annotations/create-annotation) |
| [Delete Annotation](actions/delete-annotation.md) | `DELETE /apps/annotations/:annotation_id` | [docs](https://docs.dify.ai/api-reference/annotations/delete-annotation) |
| [Delete Conversation](actions/delete-conversation.md) | `DELETE /conversations/:conversation_id` | [docs](https://docs.dify.ai/api-reference/conversations/delete-conversation) |
| [Download File](actions/download-file.md) | `GET /files/:file_id/preview` | [docs](https://docs.dify.ai/api-reference/files/download-file) |
| [Get Annotation Reply Job Status](actions/get-annotation-reply-job-status.md) | `GET /apps/annotation-reply/:action/status/:job_id` | [docs](https://docs.dify.ai/api-reference/annotations/get-annotation-reply-job-status) |
| [Get App Info](actions/get-app-info.md) | `GET /info` | [docs](https://docs.dify.ai/api-reference/applications/get-app-info) |
| [Get App Meta](actions/get-app-meta.md) | `GET /meta` | [docs](https://docs.dify.ai/api-reference/applications/get-app-meta) |
| [Get App Parameters](actions/get-app-parameters.md) | `GET /parameters` | [docs](https://docs.dify.ai/api-reference/applications/get-app-parameters) |
| [Get App WebApp Settings](actions/get-app-webapp-settings.md) | `GET /site` | [docs](https://docs.dify.ai/api-reference/applications/get-app-webapp-settings) |
| [Get End User Info](actions/get-end-user-info.md) | `GET /end-users/:end_user_id` | [docs](https://docs.dify.ai/api-reference/end-users/get-end-user-info) |
| [Get Next Suggested Questions](actions/get-next-suggested-questions.md) | `GET /messages/:message_id/suggested` | [docs](https://docs.dify.ai/api-reference/chats/get-next-suggested-questions) |
| [Get Workflow Run Detail](actions/get-workflow-run-detail.md) | `GET /workflows/run/:workflow_run_id` | [docs](https://docs.dify.ai/api-reference/workflow-runs/get-workflow-run-detail) |
| [List Annotations](actions/list-annotations.md) | `GET /apps/annotations` | [docs](https://docs.dify.ai/api-reference/annotations/list-annotations) |
| [List App Feedbacks](actions/list-app-feedbacks.md) | `GET /app/feedbacks` | [docs](https://docs.dify.ai/api-reference/feedback/list-app-feedbacks) |
| [List Conversation Messages](actions/list-conversation-messages.md) | `GET /messages` | [docs](https://docs.dify.ai/api-reference/conversations/list-conversation-messages) |
| [List Conversation Variables](actions/list-conversation-variables.md) | `GET /conversations/:conversation_id/variables` | [docs](https://docs.dify.ai/api-reference/conversations/list-conversation-variables) |
| [List Conversations](actions/list-conversations.md) | `GET /conversations` | [docs](https://docs.dify.ai/api-reference/conversations/list-conversations) |
| [List Workflow Logs](actions/list-workflow-logs.md) | `GET /workflows/logs` | [docs](https://docs.dify.ai/api-reference/workflow-runs/list-workflow-logs) |
| [Rename Conversation](actions/rename-conversation.md) | `POST /conversations/:conversation_id/name` | [docs](https://docs.dify.ai/api-reference/conversations/rename-conversation) |
| [Send Chat Message](actions/send-chat-message.md) | `POST /chat-messages` | [docs](https://docs.dify.ai/api-reference/chats/send-chat-message) |
| [Stop Chat Message Generation](actions/stop-chat-message-generation.md) | `POST /chat-messages/:task_id/stop` | [docs](https://docs.dify.ai/api-reference/chats/stop-chat-message-generation) |
| [Submit Message Feedback](actions/submit-message-feedback.md) | `POST /messages/:message_id/feedbacks` | [docs](https://docs.dify.ai/api-reference/feedback/submit-message-feedback) |
| [Update Annotation](actions/update-annotation.md) | `PUT /apps/annotations/:annotation_id` | [docs](https://docs.dify.ai/api-reference/annotations/update-annotation) |
| [Update Conversation Variable](actions/update-conversation-variable.md) | `PUT /conversations/:conversation_id/variables/:variable_id` | [docs](https://docs.dify.ai/api-reference/conversations/update-conversation-variable) |
| [Upload File](actions/upload-file.md) | `POST /files/upload` | [docs](https://docs.dify.ai/api-reference/files/upload-file) |
