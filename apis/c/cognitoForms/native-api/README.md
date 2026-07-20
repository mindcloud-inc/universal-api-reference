# Cognito Forms: Native API Reference

A consolidated summary of Cognito Forms's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://www.cognitoforms.com/support/475/data-integration/cognito-forms-api
- **OpenAPI specification:** https://static.cognitoforms.com/api-reference/CognitoFormsOpenAPI.json
- **API base URL:** `https://www.cognitoforms.com/api`

## Authentication

### API Key

Use a Cognito Forms API key for REST API access.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.cognitoforms.com/support/478/data-integration/cognito-forms-api/using-an-api-key)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Entry](actions/create-entry.md) | `POST /forms/:formId/entries` | [docs](https://www.cognitoforms.com/support/476/data-integration/cognito-forms-api/rest-api-reference#tag/entries/post/forms/{formId}/entries) |
| [Create Internal Entry](actions/create-internal-entry.md) | `POST /forms/:formId/entries` | [docs](https://www.cognitoforms.com/support/476/data-integration/cognito-forms-api/rest-api-reference#tag/entries/post/forms/{formId}/entries) |
| [Create Public Entry](actions/create-public-entry.md) | `POST /forms/:formId/entries` | [docs](https://www.cognitoforms.com/support/476/data-integration/cognito-forms-api/rest-api-reference#tag/entries/post/forms/{formId}/entries) |
| [Create Reviewer Entry](actions/create-reviewer-entry.md) | `POST /forms/:formId/entries` | [docs](https://www.cognitoforms.com/support/476/data-integration/cognito-forms-api/rest-api-reference#tag/entries/post/forms/{formId}/entries) |
| [Delete Entry](actions/delete-entry.md) | `DELETE /forms/:formId/entries/:entryId` | [docs](https://www.cognitoforms.com/support/476/data-integration/cognito-forms-api/rest-api-reference#tag/entries/delete/forms/{formId}/entries/{entryId}) |
| [Get Document](actions/get-document.md) | `GET /forms/:formId/entries/:entryId/documents/:templateId` | [docs](https://www.cognitoforms.com/support/476/data-integration/cognito-forms-api/rest-api-reference#tag/entries/get/forms/{formId}/entries/{entryId}/documents/{templateId}) |
| [Get Entry](actions/get-entry.md) | `GET /forms/:formId/entries/:entryId` | [docs](https://www.cognitoforms.com/support/476/data-integration/cognito-forms-api/rest-api-reference#tag/entries/get/forms/{formId}/entries/{entryId}) |
| [Get File](actions/get-file.md) | `GET /forms/:formId/entries/:entryId/files/:fileId` | [docs](https://www.cognitoforms.com/support/476/data-integration/cognito-forms-api/rest-api-reference#tag/entries/get/forms/{formId}/entries/{entryId}/files/{fileId}) |
| [Get Form Input Schema](actions/get-form-input-schema.md) | `GET /forms/:formId/schema` | [docs](https://www.cognitoforms.com/support/476/data-integration/cognito-forms-api/rest-api-reference#tag/forms/get/forms/{formId}/schema) |
| [Get Form Input Schema With Links](actions/get-form-input-schema-with-links.md) | `GET /forms/:formId/schema` | [docs](https://www.cognitoforms.com/support/476/data-integration/cognito-forms-api/rest-api-reference#tag/forms/get/forms/{formId}/schema) |
| [Get Form Schema](actions/get-form-schema.md) | `GET /forms/:formId/schema` | [docs](https://www.cognitoforms.com/support/476/data-integration/cognito-forms-api/rest-api-reference#tag/forms/get/forms/{formId}/schema) |
| [Get Form Schema With Links](actions/get-form-schema-with-links.md) | `GET /forms/:formId/schema` | [docs](https://www.cognitoforms.com/support/476/data-integration/cognito-forms-api/rest-api-reference#tag/forms/get/forms/{formId}/schema) |
| [Get Import Status](actions/get-import-status.md) | `GET /forms/:formId/import-status/:importId` | [docs](https://www.cognitoforms.com/support/476/data-integration/cognito-forms-api/rest-api-reference#tag/entries/get/forms/{formId}/import-status/{importId}) |
| [Import Entries Create New](actions/import-entries-create-new.md) | `POST /forms/:formId/import-entries` | [docs](https://www.cognitoforms.com/support/476/data-integration/cognito-forms-api/rest-api-reference#tag/entries/post/forms/{formId}/import-entries) |
| [Import Entries Sync Entries](actions/import-entries-sync-entries.md) | `POST /forms/:formId/import-entries` | [docs](https://www.cognitoforms.com/support/476/data-integration/cognito-forms-api/rest-api-reference#tag/entries/post/forms/{formId}/import-entries) |
| [Import Entries Update Existing](actions/import-entries-update-existing.md) | `POST /forms/:formId/import-entries` | [docs](https://www.cognitoforms.com/support/476/data-integration/cognito-forms-api/rest-api-reference#tag/entries/post/forms/{formId}/import-entries) |
| [List Forms](actions/list-forms.md) | `GET /forms` | [docs](https://www.cognitoforms.com/support/476/data-integration/cognito-forms-api/rest-api-reference#tag/forms/get/forms) |
| [List View Entries](actions/list-view-entries.md) | `GET /odata/Forms(:formId)/Views(:viewId)/Entries` | [docs](https://www.cognitoforms.com/support/496/data-integration/cognito-forms-api/odata-reference#tag/entries/get/Forms({formId})/Views({viewId})/Entries) |
| [List View Entries Select Fields](actions/list-view-entries-select-fields.md) | `GET /odata/Forms(:formId)/Views(:viewId)/Entries` | [docs](https://www.cognitoforms.com/support/496/data-integration/cognito-forms-api/odata-reference#tag/entries/get/Forms({formId})/Views({viewId})/Entries) |
| [List View Entries Select Fields With Count](actions/list-view-entries-select-fields-with-count.md) | `GET /odata/Forms(:formId)/Views(:viewId)/Entries` | [docs](https://www.cognitoforms.com/support/496/data-integration/cognito-forms-api/odata-reference#tag/entries/get/Forms({formId})/Views({viewId})/Entries) |
| [List View Entries With Count](actions/list-view-entries-with-count.md) | `GET /odata/Forms(:formId)/Views(:viewId)/Entries` | [docs](https://www.cognitoforms.com/support/496/data-integration/cognito-forms-api/odata-reference#tag/entries/get/Forms({formId})/Views({viewId})/Entries) |
| [Set Public Link Availability](actions/set-public-link-availability.md) | `POST /forms/:formId/public-link-availability` | [docs](https://www.cognitoforms.com/support/476/data-integration/cognito-forms-api/rest-api-reference#tag/forms/post/forms/{formId}/public-link-availability) |
| [Set Public Link Availability Window](actions/set-public-link-availability-window.md) | `POST /forms/:formId/public-link-availability` | [docs](https://www.cognitoforms.com/support/476/data-integration/cognito-forms-api/rest-api-reference#tag/forms/post/forms/{formId}/public-link-availability) |
| [Set Public Link End Availability](actions/set-public-link-end-availability.md) | `POST /forms/:formId/public-link-availability` | [docs](https://www.cognitoforms.com/support/476/data-integration/cognito-forms-api/rest-api-reference#tag/forms/post/forms/{formId}/public-link-availability) |
| [Set Public Link Start Availability](actions/set-public-link-start-availability.md) | `POST /forms/:formId/public-link-availability` | [docs](https://www.cognitoforms.com/support/476/data-integration/cognito-forms-api/rest-api-reference#tag/forms/post/forms/{formId}/public-link-availability) |
| [Set Public Link Unavailable Message](actions/set-public-link-unavailable-message.md) | `POST /forms/:formId/public-link-availability` | [docs](https://www.cognitoforms.com/support/476/data-integration/cognito-forms-api/rest-api-reference#tag/forms/post/forms/{formId}/public-link-availability) |
| [Update Entry](actions/update-entry.md) | `PATCH /forms/:formId/entries/:entryId` | [docs](https://www.cognitoforms.com/support/476/data-integration/cognito-forms-api/rest-api-reference#tag/entries/patch/forms/{formId}/entries/{entryId}) |
| [Update Entry As Internal](actions/update-entry-as-internal.md) | `PATCH /forms/:formId/entries/:entryId` | [docs](https://www.cognitoforms.com/support/476/data-integration/cognito-forms-api/rest-api-reference#tag/entries/patch/forms/{formId}/entries/{entryId}) |
| [Update Entry As Reviewer](actions/update-entry-as-reviewer.md) | `PATCH /forms/:formId/entries/:entryId` | [docs](https://www.cognitoforms.com/support/476/data-integration/cognito-forms-api/rest-api-reference#tag/entries/patch/forms/{formId}/entries/{entryId}) |
| [Upload File](actions/upload-file.md) | `POST /files` | [docs](https://www.cognitoforms.com/support/476/data-integration/cognito-forms-api/rest-api-reference#tag/entries/post/files) |
