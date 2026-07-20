# <img src="https://images.mindcloud.co/apps/icons/trint_1774644866773.png" alt="Trint logo" width="28" height="28"> Trint: Universal API

AI transcription and translation platform for converting audio, video, and live conversations into searchable transcripts, exports, captions, and realtime feeds.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/trint/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://trint.com
- **Vendor API docs:** https://dev.trint.com/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Files](actions/list-files.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trint/latest/actions/list-files?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Export File

| Action | Method | Description |
| --- | --- | --- |
| [Export Comments as CSV](actions/export-comments-as-csv.md) | GET | Exports file comments as CSV from Trint. |
| [Export File as Avid DS](actions/export-file-as-avid-ds.md) | GET | Exports a file as Avid DS from Trint. |
| [Export File as DOCX](actions/export-file-as-docx.md) | GET | Exports a file as DOCX from Trint. |
| [Export File as EDL](actions/export-file-as-edl.md) | GET | Exports a file as EDL from Trint. |
| [Export File as HTML](actions/export-file-as-html.md) | GET | Exports a file as HTML from Trint. |
| [Export File as JSON](actions/export-file-as-json.md) | GET | Exports a file as JSON from Trint. |
| [Export File as Premiere XML](actions/export-file-as-premiere-xml.md) | GET | Exports a file as Premiere XML from Trint. |
| [Export File as Spruce STL](actions/export-file-as-spruce-stl.md) | GET | Exports a file as Spruce STL from Trint. |
| [Export File as SubRip SRT](actions/export-file-as-subrip-srt.md) | GET | Exports a file as SubRip SRT from Trint. |
| [Export File as Telestream Vantage XML](actions/export-file-as-telestream-vantage-xml.md) | GET | Exports a file as Telestream Vantage XML from Trint. |
| [Export File as Text](actions/export-file-as-text.md) | GET | Exports a file as text from Trint. |
| [Export File as WebVTT](actions/export-file-as-webvtt.md) | GET | Exports a file as WebVTT from Trint. |
| [Export File as XML](actions/export-file-as-xml.md) | GET | Exports a file as XML from Trint. |
| [Export Full Transcript as CSV](actions/export-full-transcript-as-csv.md) | GET | Exports a full transcript as CSV from Trint. |
| [Export Highlights as CSV](actions/export-highlights-as-csv.md) | GET | Exports file highlights as CSV from Trint. |
| [Export Markers as CSV](actions/export-markers-as-csv.md) | GET | Exports file markers as CSV from Trint. |

### Folder

| Action | Method | Description |
| --- | --- | --- |
| [Create Folder](actions/create-folder.md) | POST | Creates a new folder in Trint. |
| [List Folders](actions/list-folders.md) | GET | Retrieves folders from your Trint account. |
| [Retrieve Folder](actions/retrieve-folder.md) | GET | Retrieves a folder from your Trint account. |

### Push Stream

| Action | Method | Description |
| --- | --- | --- |
| [Create Push Stream](actions/create-push-stream.md) | POST | Creates a new push stream in Trint. |

### Realtime Transcript

| Action | Method | Description |
| --- | --- | --- |
| [Get Realtime Status](actions/get-realtime-status.md) | GET | Retrieves realtime transcript status from Trint. |
| [Start New Realtime Transcript](actions/start-new-realtime-transcript.md) | PUT | Starts a new realtime transcript in Trint. |
| [Stop Realtime Transcript](actions/stop-realtime-transcript.md) | DELETE | Stops a realtime transcript in Trint. |

### Scim Group

| Action | Method | Description |
| --- | --- | --- |
| [List SCIM Groups](actions/list-scim-groups.md) | GET | Retrieves SCIM groups from Trint. |

### Scim User

| Action | Method | Description |
| --- | --- | --- |
| [List SCIM Users](actions/list-scim-users.md) | GET | Retrieves SCIM users from Trint. |
| [Search SCIM Users with Filter](actions/search-scim-users-with-filter.md) | GET | Finds SCIM users in Trint by filter. |

### Shared Drive

| Action | Method | Description |
| --- | --- | --- |
| [List Shared Drives](actions/list-shared-drives.md) | GET | Retrieves shared drives from your Trint account. |
| [Retrieve Shared Drive](actions/retrieve-shared-drive.md) | GET | Retrieves a shared drive from your Trint account. |

### Story Export File

| Action | Method | Description |
| --- | --- | --- |
| [Export Story Builder as DOCX](actions/export-story-builder-as-docx.md) | GET | Exports a Story Builder file as DOCX from Trint. |
| [Export Story Builder as EDL](actions/export-story-builder-as-edl.md) | GET | Exports a Story Builder file as EDL from Trint. |
| [Export Story Builder as Premiere XML](actions/export-story-builder-as-premiere-xml.md) | GET | Exports a Story Builder file as Premiere XML from Trint. |

### Transcript

| Action | Method | Description |
| --- | --- | --- |
| [List Files](actions/list-files.md) | GET | Retrieves files from your Trint account. |
| [Retrieve File](actions/retrieve-file.md) | GET | Retrieves a file from your Trint account. |
| [Upload and Transcribe](actions/upload-and-transcribe.md) | POST | Uploads and transcribes a file in Trint. |

### Translation

| Action | Method | Description |
| --- | --- | --- |
| [Create Translation](actions/create-translation.md) | POST | Creates a new translation in Trint. |
| [Delete Translation](actions/delete-translation.md) | DELETE | Deletes an existing translation from Trint. |
| [List Translations](actions/list-translations.md) | GET | Retrieves translations from your Trint account. |

### Translation Language

| Action | Method | Description |
| --- | --- | --- |
| [List Translation Languages](actions/list-translation-languages.md) | GET | Retrieves translation languages from Trint. |

### Webhook Endpoint

| Action | Method | Description |
| --- | --- | --- |
| [Deregister Webhook Endpoint](actions/deregister-webhook-endpoint.md) | DELETE | Deregisters a webhook endpoint from Trint. |
| [Register Webhook Endpoint](actions/register-webhook-endpoint.md) | PUT | Registers a webhook endpoint in Trint. |

