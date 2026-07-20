# Trint: Native API Reference

A consolidated summary of Trint's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://dev.trint.com/reference
- **API base URL:** `https://api.trint.com`

## Authentication

### Basic

Use your Trint Api Key Id as the username and your Api Key Secret as the password.

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

[Official authentication documentation](https://dev.trint.com/docs/trint-api-keys)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `accept` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 100; accepted range 1–1000). Use `skip` in the query string as the record offset; numbering starts at 0.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Folder](actions/create-folder.md) | `POST /folders/` | [docs](https://dev.trint.com/reference/page-1) |
| [Create Push Stream](actions/create-push-stream.md) | `POST /transcripts/realtime/push` | [docs](https://dev.trint.com/reference/create-push-stream) |
| [Create Translation](actions/create-translation.md) | `POST https://translation.api.trint.com/` | [docs](https://dev.trint.com/reference/create-translation) |
| [Delete Translation](actions/delete-translation.md) | `DELETE https://translation.api.trint.com/` | [docs](https://dev.trint.com/reference/delete-translation) |
| [Deregister Webhook Endpoint](actions/deregister-webhook-endpoint.md) | `DELETE /callbacks/transcript/` | [docs](https://dev.trint.com/reference/de-register-webook) |
| [Export Comments as CSV](actions/export-comments-as-csv.md) | `GET /export/csv/comments/:trintId` | [docs](https://dev.trint.com/reference/csvcommentstrint-id) |
| [Export File as Avid DS](actions/export-file-as-avid-ds.md) | `GET /export/avid-ds/:trintId` | [docs](https://dev.trint.com/reference/avid-dstrint-id) |
| [Export File as DOCX](actions/export-file-as-docx.md) | `GET /export/docx/:trintId` | [docs](https://dev.trint.com/reference/transcript-docx) |
| [Export File as EDL](actions/export-file-as-edl.md) | `GET /export/edl/:trintId` | [docs](https://dev.trint.com/reference/transcript-edl) |
| [Export File as HTML](actions/export-file-as-html.md) | `GET /export/html/:trintId` | [docs](https://dev.trint.com/reference/html) |
| [Export File as JSON](actions/export-file-as-json.md) | `GET /export/json/:trintId` | [docs](https://dev.trint.com/reference/jsontrint-id) |
| [Export File as Premiere XML](actions/export-file-as-premiere-xml.md) | `GET /export/premiere-xml/:trintId` | [docs](https://dev.trint.com/reference/premiere-xml) |
| [Export File as Spruce STL](actions/export-file-as-spruce-stl.md) | `GET /export/spruce-stl/:trintId` | [docs](https://dev.trint.com/reference/spruce-stltrint-id) |
| [Export File as SubRip SRT](actions/export-file-as-subrip-srt.md) | `GET /export/srt/:trintId` | [docs](https://dev.trint.com/reference/testinput-1) |
| [Export File as Telestream Vantage XML](actions/export-file-as-telestream-vantage-xml.md) | `GET /export/vantage-xml/:trintId` | [docs](https://dev.trint.com/reference/telestream-vantage-xml) |
| [Export File as Text](actions/export-file-as-text.md) | `GET /export/text/:trintId` | [docs](https://dev.trint.com/reference/text) |
| [Export File as WebVTT](actions/export-file-as-webvtt.md) | `GET /export/webvtt/:trintId` | [docs](https://dev.trint.com/reference/webvtttrint-id) |
| [Export File as XML](actions/export-file-as-xml.md) | `GET /export/xml/:trintId` | [docs](https://dev.trint.com/reference/xmltrint-id) |
| [Export Full Transcript as CSV](actions/export-full-transcript-as-csv.md) | `GET /export/csv/full/:trintId` | [docs](https://dev.trint.com/reference/full-transcript-csv) |
| [Export Highlights as CSV](actions/export-highlights-as-csv.md) | `GET /export/csv/highlights/:trintId` | [docs](https://dev.trint.com/reference/csvhighlightstrint-id) |
| [Export Markers as CSV](actions/export-markers-as-csv.md) | `GET /export/csv/markers/:trintId` | [docs](https://dev.trint.com/reference/markers-csv) |
| [Export Story Builder as DOCX](actions/export-story-builder-as-docx.md) | `GET /export/story-builder/docx/:fileId` | [docs](https://dev.trint.com/reference/story-builder-docx) |
| [Export Story Builder as EDL](actions/export-story-builder-as-edl.md) | `GET /export/story-builder/edl/:fileId` | [docs](https://dev.trint.com/reference/story-builder-edl) |
| [Export Story Builder as Premiere XML](actions/export-story-builder-as-premiere-xml.md) | `GET /export/story-builder/project_xml/:fileId` | [docs](https://dev.trint.com/reference/premiere-xml-copy) |
| [Get Realtime Status](actions/get-realtime-status.md) | `GET /transcripts/realtime/:trintId` | [docs](https://dev.trint.com/reference/get-realtime-status) |
| [List Files](actions/list-files.md) | `GET /transcripts/` | [docs](https://dev.trint.com/reference/page) |
| [List Folders](actions/list-folders.md) | `GET /folders/` | [docs](https://dev.trint.com/reference/folders) |
| [List SCIM Groups](actions/list-scim-groups.md) | `GET https://scim.trint.com/v2/Groups` | [docs](https://dev.trint.com/reference/searchgroupsviaget) |
| [List SCIM Users](actions/list-scim-users.md) | `GET https://scim.trint.com/v2/Users` | [docs](https://dev.trint.com/reference/searchusersviaget) |
| [List Shared Drives](actions/list-shared-drives.md) | `GET /workspaces/` | [docs](https://dev.trint.com/reference/list-workspaces) |
| [List Translation Languages](actions/list-translation-languages.md) | `GET https://translation.api.trint.com/translation-languages` | [docs](https://dev.trint.com/reference/translation-languages) |
| [List Translations](actions/list-translations.md) | `GET https://translation.api.trint.com/` | [docs](https://dev.trint.com/reference/get-translations) |
| [Register Webhook Endpoint](actions/register-webhook-endpoint.md) | `PUT /callbacks/transcript/` | [docs](https://dev.trint.com/reference/register-webhook-endpoint) |
| [Retrieve File](actions/retrieve-file.md) | `GET /transcripts/file/:id` | [docs](https://dev.trint.com/reference/get-file) |
| [Retrieve Folder](actions/retrieve-folder.md) | `GET /folders/folder` | [docs](https://dev.trint.com/reference/retrieve-folder) |
| [Retrieve Shared Drive](actions/retrieve-shared-drive.md) | `GET /workspaces/workspace` | [docs](https://dev.trint.com/reference/retrieve-shared-drive) |
| [Search SCIM Users with Filter](actions/search-scim-users-with-filter.md) | `POST https://scim.trint.com/v2/Users/.search` | [docs](https://dev.trint.com/reference/searchusersviapost) |
| [Start New Realtime Transcript](actions/start-new-realtime-transcript.md) | `PUT /transcripts/realtime/` | [docs](https://dev.trint.com/reference/start-new-realtime-transcript) |
| [Stop Realtime Transcript](actions/stop-realtime-transcript.md) | `DELETE /transcripts/realtime/` | [docs](https://dev.trint.com/reference/stop-realtime-transcript) |
| [Upload and Transcribe](actions/upload-and-transcribe.md) | `POST https://upload.trint.com/` | [docs](https://dev.trint.com/reference/upload) |
