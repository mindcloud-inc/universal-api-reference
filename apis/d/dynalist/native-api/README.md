# Dynalist: Native API Reference

A consolidated summary of Dynalist's API configuration and 16 documented operations, with links to official documentation.

- **Official docs:** https://apidocs.dynalist.io/
- **API base URL:** `https://dynalist.io/api/v1/`

## Authentication

### API Secret Token

Dynalist API secret token from the Dynalist developer page.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://apidocs.dynalist.io/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (16 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Batch Edit Document Nodes](actions/batch-edit-document-nodes.md) | `POST /doc/edit` | [docs](https://apidocs.dynalist.io/#make-change-to-the-content-of-a-document) |
| [Batch Edit Files And Folders](actions/batch-edit-files-and-folders.md) | `POST /file/edit` | [docs](https://apidocs.dynalist.io/#make-changes-to-documents-and-folders) |
| [Check Documents For Updates](actions/check-documents-for-updates.md) | `POST /doc/check_for_updates` | [docs](https://apidocs.dynalist.io/#check-if-documents-has-been-updated) |
| [Create File](actions/create-file.md) | `POST /file/edit` | [docs](https://apidocs.dynalist.io/#make-changes-to-documents-and-folders) |
| [Delete Node](actions/delete-node.md) | `POST /doc/edit` | [docs](https://apidocs.dynalist.io/#make-change-to-the-content-of-a-document) |
| [Get Preference](actions/get-preference.md) | `POST /pref/get` | [docs](https://apidocs.dynalist.io/#get-preference) |
| [Insert Node](actions/insert-node.md) | `POST /doc/edit` | [docs](https://apidocs.dynalist.io/#make-change-to-the-content-of-a-document) |
| [List Documents And Folders](actions/list-documents-and-folders.md) | `POST /file/list` | [docs](https://apidocs.dynalist.io/#get-all-documents-and-folders) |
| [Move File](actions/move-file.md) | `POST /file/edit` | [docs](https://apidocs.dynalist.io/#make-changes-to-documents-and-folders) |
| [Move Node](actions/move-node.md) | `POST /doc/edit` | [docs](https://apidocs.dynalist.io/#make-change-to-the-content-of-a-document) |
| [Read Document](actions/read-document.md) | `POST /doc/read` | [docs](https://apidocs.dynalist.io/#get-content-of-a-document) |
| [Rename File](actions/rename-file.md) | `POST /file/edit` | [docs](https://apidocs.dynalist.io/#make-changes-to-documents-and-folders) |
| [Send Item To Inbox](actions/send-item-to-inbox.md) | `POST /inbox/add` | [docs](https://apidocs.dynalist.io/#send-to-inbox) |
| [Set Preference](actions/set-preference.md) | `POST /pref/set` | [docs](https://apidocs.dynalist.io/#set-preference) |
| [Update Node](actions/update-node.md) | `POST /doc/edit` | [docs](https://apidocs.dynalist.io/#make-change-to-the-content-of-a-document) |
| [Upload File](actions/upload-file.md) | `POST /upload` | [docs](https://apidocs.dynalist.io/#upload-file-pro-only) |
