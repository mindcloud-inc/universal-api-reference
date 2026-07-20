# Voiceflow: Native API Reference

A consolidated summary of Voiceflow's API configuration and 31 documented operations, with links to official documentation.

- **Official docs:** https://docs.voiceflow.com/reference/api-overview
- **API base URL:** `https://general-runtime.voiceflow.com`

## Authentication

### API Key

Use your Voiceflow project API key.

### Credentials

- **API Key:** `apiKey` · required
- **Project ID:** `projectId` · required · ID of the Voiceflow project to target.

Send these headers with each API request:

```http
projectID: <projectId>
Authorization: <apiKey>
```

[Official authentication documentation](https://docs.voiceflow.com/api-reference/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (31 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Document](actions/create-document.md) | `POST https://realtime-api.voiceflow.com/v1alpha1/public/knowledge-base/document` | [docs](https://docs.voiceflow.com/api-reference/kbpublicapidocument/create-document) |
| [Create Transcript Evaluation](actions/create-transcript-evaluation.md) | `POST https://analytics-api.voiceflow.com/v1/transcript-evaluation` | [docs](https://docs.voiceflow.com/api-reference/transcript-evaluation/create-transcript-evaluation) |
| [Create Transcript Property](actions/create-transcript-property.md) | `POST https://analytics-api.voiceflow.com/v1/transcript-property` | [docs](https://docs.voiceflow.com/api-reference/transcript-property/create-transcript-property) |
| [Delete Conversation State](actions/delete-conversation-state.md) | `DELETE /state/user/:userId` | [docs](https://docs.voiceflow.com/api-reference/state/delete-conversation-state) |
| [Delete Document](actions/delete-document.md) | `DELETE https://realtime-api.voiceflow.com/v1alpha1/public/knowledge-base/document/:documentId` | [docs](https://docs.voiceflow.com/api-reference/kbpublicapidocument/delete-document) |
| [Delete Transcript](actions/delete-transcript.md) | `DELETE https://analytics-api.voiceflow.com/v1/transcript/:transcriptId` | [docs](https://docs.voiceflow.com/api-reference/transcript/delete-transcript) |
| [Delete Transcript Evaluation](actions/delete-transcript-evaluation.md) | `DELETE https://analytics-api.voiceflow.com/v1/transcript-evaluation/:evaluationId` | [docs](https://docs.voiceflow.com/api-reference/transcript-evaluation/delete-transcript-evaluation) |
| [Delete Transcript Property](actions/delete-transcript-property.md) | `DELETE https://analytics-api.voiceflow.com/v1/transcript-property/:propertyId` | [docs](https://docs.voiceflow.com/api-reference/transcript-property/delete-transcript-property) |
| [Delete Transcript Property Value](actions/delete-transcript-property-value.md) | `DELETE https://analytics-api.voiceflow.com/v1/transcript-property-value/transcript/:transcriptId/property/:propertyId` | [docs](https://docs.voiceflow.com/api-reference/transcript-property-value/delete-transcript-property-value) |
| [Emit Session Event](actions/emit-session-event.md) | `POST /v2/project/:projectId/session/:sessionId/event` | [docs](https://docs.voiceflow.com/api-reference/session/emit-session-event) |
| [End Transcript](actions/end-transcript.md) | `POST https://analytics-api.voiceflow.com/v1/transcript/:transcriptId/project/:projectId/end` | [docs](https://docs.voiceflow.com/api-reference/transcript/end-transcript) |
| [Fetch Project](actions/fetch-project.md) | `GET https://api.voiceflow.com/v2/versions/:versionId/export` | [docs](https://docs.voiceflow.com/api-reference/project/fetch-project) |
| [Get Conversation State](actions/get-conversation-state.md) | `GET /state/user/:userId` | [docs](https://docs.voiceflow.com/api-reference/state/get-conversation-state) |
| [Get Document](actions/get-document.md) | `GET https://realtime-api.voiceflow.com/v1alpha1/public/knowledge-base/document/:documentId` | [docs](https://docs.voiceflow.com/api-reference/kbpublicapidocument/get-document) |
| [Get Transcript](actions/get-transcript.md) | `GET https://analytics-api.voiceflow.com/v1/transcript/:transcriptId` | [docs](https://docs.voiceflow.com/api-reference/transcript/get-transcript) |
| [Get Transcript Evaluation](actions/get-transcript-evaluation.md) | `GET https://analytics-api.voiceflow.com/v1/transcript-evaluation/:evaluationId` | [docs](https://docs.voiceflow.com/api-reference/transcript-evaluation/get-transcript-evaluation) |
| [Get Transcript Property](actions/get-transcript-property.md) | `GET https://analytics-api.voiceflow.com/v1/transcript-property/:propertyId` | [docs](https://docs.voiceflow.com/api-reference/transcript-property/get-transcript-property) |
| [Interact Non-Stream](actions/interact-non-stream.md) | `POST /state/user/:userId/interact` | [docs](https://docs.voiceflow.com/api-reference/conversation/interact-non-stream) |
| [List Evaluations](actions/list-evaluations.md) | `GET https://analytics-api.voiceflow.com/v1/transcript-evaluation/project/:projectId` | [docs](https://docs.voiceflow.com/api-reference/transcript-evaluation/get-all-evaluations) |
| [List Transcript Property Values](actions/list-transcript-property-values.md) | `GET https://analytics-api.voiceflow.com/v1/transcript-property-value/transcript/:transcriptId` | [docs](https://docs.voiceflow.com/api-reference/transcript-property-value/get-all-transcript-property-values) |
| [Replace Document](actions/replace-document.md) | `PUT https://realtime-api.voiceflow.com/v1alpha1/public/knowledge-base/document/:documentId` | [docs](https://docs.voiceflow.com/api-reference/kbpublicapidocument/replace-document) |
| [Search Documents](actions/search-documents.md) | `GET https://realtime-api.voiceflow.com/v1alpha1/public/knowledge-base/document` | [docs](https://docs.voiceflow.com/api-reference/kbpublicapidocument/search-documents) |
| [Search Transcripts](actions/search-transcripts.md) | `POST https://analytics-api.voiceflow.com/v1/transcript/project/:projectId` | [docs](https://docs.voiceflow.com/api-reference/transcript/search-transcripts) |
| [Set Transcript Property Value](actions/set-transcript-property-value.md) | `POST https://analytics-api.voiceflow.com/v1/transcript-property-value` | [docs](https://docs.voiceflow.com/api-reference/transcript-property-value/set-transcript-property-value) |
| [Update Chunk Metadata](actions/update-chunk-metadata.md) | `PATCH https://realtime-api.voiceflow.com/v1alpha1/public/knowledge-base/document/:documentId/chunk/:chunkId` | [docs](https://docs.voiceflow.com/api-reference/kbpublicapidocument/update-chunk-metadata) |
| [Update Conversation State](actions/update-conversation-state.md) | `PUT /state/user/:userId` | [docs](https://docs.voiceflow.com/api-reference/state/update-conversation-state) |
| [Update Conversation Variables](actions/update-conversation-variables.md) | `PATCH /state/user/:userId/variables` | [docs](https://docs.voiceflow.com/api-reference/state/update-conversation-variables) |
| [Update Document Metadata](actions/update-document-metadata.md) | `PATCH https://realtime-api.voiceflow.com/v1alpha1/public/knowledge-base/document/:documentId` | [docs](https://docs.voiceflow.com/api-reference/kbpublicapidocument/update-document-metadata) |
| [Update Transcript Evaluation](actions/update-transcript-evaluation.md) | `PATCH https://analytics-api.voiceflow.com/v1/transcript-evaluation/:evaluationId` | [docs](https://docs.voiceflow.com/api-reference/transcript-evaluation/update-transcript-evaluation) |
| [Update Transcript Property](actions/update-transcript-property.md) | `PATCH https://analytics-api.voiceflow.com/v1/transcript-property/:propertyId` | [docs](https://docs.voiceflow.com/api-reference/transcript-property/update-transcript-property) |
| [Upload Table Document](actions/upload-table-document.md) | `POST https://realtime-api.voiceflow.com/v1alpha1/public/knowledge-base/document/upload/table` | [docs](https://docs.voiceflow.com/api-reference/kbpublicapidocument/upload-table-document) |
