# <img src="https://images.mindcloud.co/apps/icons/dify_1774455900354.png" alt="Dify logo" width="28" height="28"> Dify: Universal API

Run Dify app conversations, files, annotations, and feedback

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/dify/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 28
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://dify.ai
- **Vendor API docs:** https://docs.dify.ai/api-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get App Info](actions/get-app-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dify/latest/actions/get-app-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (28)

### Annotation

| Action | Method | Description |
| --- | --- | --- |
| [Create Annotation](actions/create-annotation.md) | POST | Creates a new annotation in Dify. |
| [Delete Annotation](actions/delete-annotation.md) | DELETE | Deletes an existing annotation from Dify. |
| [List Annotations](actions/list-annotations.md) | GET | Retrieves annotations from Dify. |
| [Update Annotation](actions/update-annotation.md) | PUT | Updates an existing annotation in Dify. |

### Annotation Reply

| Action | Method | Description |
| --- | --- | --- |
| [Configure Annotation Reply](actions/configure-annotation-reply.md) | PUT | Updates annotation reply settings in Dify. |

### Annotation Reply Job

| Action | Method | Description |
| --- | --- | --- |
| [Get Annotation Reply Job Status](actions/get-annotation-reply-job-status.md) | GET | Retrieves annotation reply job status from Dify. |

### App Feedback

| Action | Method | Description |
| --- | --- | --- |
| [List App Feedbacks](actions/list-app-feedbacks.md) | GET | Retrieves app feedback entries from Dify. |

### App Parameter

| Action | Method | Description |
| --- | --- | --- |
| [Get App Parameters](actions/get-app-parameters.md) | GET | Retrieves application parameters from Dify. |

### Application

| Action | Method | Description |
| --- | --- | --- |
| [Get App Info](actions/get-app-info.md) | GET | Retrieves application info from Dify. |
| [Get App Meta](actions/get-app-meta.md) | GET | Retrieves application metadata from Dify. |

### Audio

| Action | Method | Description |
| --- | --- | --- |
| [Convert Text to Audio](actions/convert-text-to-audio.md) | POST | Creates audio from text in Dify. |

### Chat Message

| Action | Method | Description |
| --- | --- | --- |
| [Send Chat Message](actions/send-chat-message.md) | POST | Creates a chat message in Dify. |
| [Stop Chat Message Generation](actions/stop-chat-message-generation.md) | PUT | Stops chat message generation in Dify. |

### Conversation

| Action | Method | Description |
| --- | --- | --- |
| [Delete Conversation](actions/delete-conversation.md) | DELETE | Deletes an existing conversation from Dify. |
| [List Conversations](actions/list-conversations.md) | GET | Retrieves conversations from Dify. |
| [Rename Conversation](actions/rename-conversation.md) | PUT | Updates a conversation name in Dify. |

### Conversation Variable

| Action | Method | Description |
| --- | --- | --- |
| [List Conversation Variables](actions/list-conversation-variables.md) | GET | Retrieves conversation variables from Dify. |
| [Update Conversation Variable](actions/update-conversation-variable.md) | PUT | Updates an existing conversation variable in Dify. |

### End User

| Action | Method | Description |
| --- | --- | --- |
| [Get End User Info](actions/get-end-user-info.md) | GET | Retrieves end-user details from Dify. |

### File

| Action | Method | Description |
| --- | --- | --- |
| [Download File](actions/download-file.md) | GET | Retrieves a file preview or download from Dify. |
| [Upload File](actions/upload-file.md) | POST | Uploads a file to Dify. |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [List Conversation Messages](actions/list-conversation-messages.md) | GET | Retrieves conversation messages from Dify. |

### Message Feedback

| Action | Method | Description |
| --- | --- | --- |
| [Submit Message Feedback](actions/submit-message-feedback.md) | POST | Creates message feedback in Dify. |

### Suggested Question

| Action | Method | Description |
| --- | --- | --- |
| [Get Next Suggested Questions](actions/get-next-suggested-questions.md) | GET | Retrieves suggested questions from Dify. |

### Transcription

| Action | Method | Description |
| --- | --- | --- |
| [Convert Audio to Text](actions/convert-audio-to-text.md) | POST | Creates a text transcription from audio in Dify. |

### Webapp Setting

| Action | Method | Description |
| --- | --- | --- |
| [Get App WebApp Settings](actions/get-app-webapp-settings.md) | GET | Retrieves WebApp settings from Dify. |

### Workflow Log

| Action | Method | Description |
| --- | --- | --- |
| [List Workflow Logs](actions/list-workflow-logs.md) | GET | Retrieves workflow logs from Dify. |

### Workflow Run

| Action | Method | Description |
| --- | --- | --- |
| [Get Workflow Run Detail](actions/get-workflow-run-detail.md) | GET | Retrieves workflow run details from Dify. |

