# <img src="https://images.mindcloud.co/apps/icons/idq-metg2nr-1774551428911_1774551433490.jpeg" alt="Voiceflow logo" width="28" height="28"> Voiceflow: Universal API

Build, deploy, and manage conversational AI agents

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/voiceflow/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 31
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.voiceflow.com
- **Vendor API docs:** https://docs.voiceflow.com/reference/api-overview

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Conversation State](actions/get-conversation-state.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/voiceflow/latest/actions/get-conversation-state?connectionId=$CONNECTION_ID&userId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (31)

### Conversation

| Action | Method | Description |
| --- | --- | --- |
| [Delete Conversation State](actions/delete-conversation-state.md) | DELETE | Deletes a user's conversation state from Voiceflow. |
| [Get Conversation State](actions/get-conversation-state.md) | GET | Retrieves a user's conversation state from Voiceflow. |
| [Interact Non-Stream](actions/interact-non-stream.md) | POST | Sends a conversation action to Voiceflow and returns traces. |
| [Update Conversation State](actions/update-conversation-state.md) | PUT | Updates a user's conversation state in Voiceflow. |
| [Update Conversation Variables](actions/update-conversation-variables.md) | PUT | Updates a user's conversation variables in Voiceflow. |

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Create Document](actions/create-document.md) | POST | Creates a knowledge base document in Voiceflow. |
| [Get Document](actions/get-document.md) | GET | Retrieves a knowledge base document from Voiceflow. |
| [Search Documents](actions/search-documents.md) | GET | Finds knowledge base documents in Voiceflow. |
| [Upload Table Document](actions/upload-table-document.md) | POST | Uploads a table document to Voiceflow's knowledge base. |

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Replace Document](actions/replace-document.md) | PUT | Replaces a knowledge base document in Voiceflow. |
| [Update Chunk Metadata](actions/update-chunk-metadata.md) | PUT | Updates chunk metadata in Voiceflow's knowledge base. |
| [Update Document Metadata](actions/update-document-metadata.md) | PUT | Updates document metadata in Voiceflow's knowledge base. |

### Knowledge Base Document

| Action | Method | Description |
| --- | --- | --- |
| [Delete Document](actions/delete-document.md) | DELETE | Deletes a knowledge base document from Voiceflow. |

### Project Export

| Action | Method | Description |
| --- | --- | --- |
| [Fetch Project](actions/fetch-project.md) | GET | Retrieves exported project files from Voiceflow. |

### Session

| Action | Method | Description |
| --- | --- | --- |
| [Emit Session Event](actions/emit-session-event.md) | POST | Sends an event to an active Voiceflow session. |

### Transcript

| Action | Method | Description |
| --- | --- | --- |
| [Get Transcript](actions/get-transcript.md) | GET | Retrieves a transcript and its results from Voiceflow. |

### Transcript Evaluation

| Action | Method | Description |
| --- | --- | --- |
| [Create Transcript Evaluation](actions/create-transcript-evaluation.md) | POST | Creates a new transcript evaluation in Voiceflow. |

### Transcript Evaluation List

| Action | Method | Description |
| --- | --- | --- |
| [List Evaluations](actions/list-evaluations.md) | GET | Retrieves all transcript evaluations from Voiceflow. |

### Transcript Property

| Action | Method | Description |
| --- | --- | --- |
| [Create Transcript Property](actions/create-transcript-property.md) | POST | Creates a new transcript property in Voiceflow. |
| [Get Transcript Property](actions/get-transcript-property.md) | GET | Retrieves a transcript property from Voiceflow. |

### Transcript Property Value

| Action | Method | Description |
| --- | --- | --- |
| [Set Transcript Property Value](actions/set-transcript-property-value.md) | POST | Sets a transcript property value in Voiceflow. |

### Transcript Search

| Action | Method | Description |
| --- | --- | --- |
| [Search Transcripts](actions/search-transcripts.md) | GET | Finds transcripts in Voiceflow by project criteria. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Delete Transcript](actions/delete-transcript.md) | DELETE | Deletes an existing transcript from Voiceflow. |
| [Delete Transcript Evaluation](actions/delete-transcript-evaluation.md) | DELETE | Deletes an existing transcript evaluation from Voiceflow. |
| [Delete Transcript Property](actions/delete-transcript-property.md) | DELETE | Deletes an existing transcript property from Voiceflow. |
| [Delete Transcript Property Value](actions/delete-transcript-property-value.md) | DELETE | Deletes a transcript property value from Voiceflow. |
| [End Transcript](actions/end-transcript.md) | PUT | Marks a Voiceflow transcript as complete. |
| [Get Transcript Evaluation](actions/get-transcript-evaluation.md) | GET | Retrieves a transcript evaluation from Voiceflow. |
| [List Transcript Property Values](actions/list-transcript-property-values.md) | GET | Retrieves transcript property values from Voiceflow. |
| [Update Transcript Evaluation](actions/update-transcript-evaluation.md) | PUT | Updates an existing transcript evaluation in Voiceflow. |
| [Update Transcript Property](actions/update-transcript-property.md) | PUT | Updates an existing transcript property in Voiceflow. |

