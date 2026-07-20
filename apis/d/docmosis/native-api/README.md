# Docmosis: Native API Reference

A consolidated summary of Docmosis's API configuration and 21 documented operations, with links to official documentation.

- **Official docs:** https://apidocs.docmosis.com/cloud/dws4/
- **OpenAPI specification:** https://us1.dws4.docmosis.com/api/openapi.json
- **API base URL:** `{baseUrl}`

## Authentication

### API Key

Connect with a Docmosis Cloud access key and the matching region base URL.

### Credentials

- **API Key:** `apiKey` · required
- **Base URL:** `baseUrl` · required · Docmosis API base URL for the processing location that stores your templates and images.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://resources.docmosis.com/faq/cloud-api-urls-and-access-keys)

## API conventions

Responses from this API use JSON.

## Endpoints (21 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Upload Template Batch](actions/cancel-upload-template-batch.md) | `POST /uploadTemplateBatchCancel` | [docs](https://resources.docmosis.com/Documentation/Cloud/DWS4/Cloud-Web-Services-Guide-DWS4.pdf#page=46) |
| [Convert File](actions/convert-file.md) | `POST /convert` | [docs](https://resources.docmosis.com/Documentation/Cloud/DWS4/Cloud-Web-Services-Guide-DWS4.pdf#page=53) |
| [Delete Image](actions/delete-image.md) | `POST /deleteImage` | [docs](https://resources.docmosis.com/Documentation/Cloud/DWS4/Cloud-Web-Services-Guide-DWS4.pdf#page=51) |
| [Delete Template](actions/delete-template.md) | `POST /deleteTemplate` | [docs](https://resources.docmosis.com/Documentation/Cloud/DWS4/Cloud-Web-Services-Guide-DWS4.pdf#page=39) |
| [Get Environment Ready Status](actions/get-environment-ready-status.md) | `POST /environment/ready` | [docs](https://resources.docmosis.com/Documentation/Cloud/DWS4/Cloud-Web-Services-Guide-DWS4.pdf#page=62) |
| [Get Environment Summary](actions/get-environment-summary.md) | `POST /environment/summary` | [docs](https://resources.docmosis.com/Documentation/Cloud/DWS4/Cloud-Web-Services-Guide-DWS4.pdf#page=63) |
| [Get Image](actions/get-image.md) | `POST /getImage` | [docs](https://resources.docmosis.com/Documentation/Cloud/DWS4/Cloud-Web-Services-Guide-DWS4.pdf#page=52) |
| [Get Render Queue](actions/get-render-queue.md) | `POST /getRenderQueue` | [docs](https://resources.docmosis.com/Documentation/Cloud/DWS4/Cloud-Web-Services-Guide-DWS4.pdf#page=59) |
| [Get Render Tags](actions/get-render-tags.md) | `POST /getRenderTags` | [docs](https://resources.docmosis.com/Documentation/Cloud/DWS4/Cloud-Web-Services-Guide-DWS4.pdf#page=54) |
| [Get Template](actions/get-template.md) | `POST /getTemplate` | [docs](https://resources.docmosis.com/Documentation/Cloud/DWS4/Cloud-Web-Services-Guide-DWS4.pdf#page=32) |
| [Get Template Details](actions/get-template-details.md) | `POST /getTemplateDetails` | [docs](https://resources.docmosis.com/Documentation/Cloud/DWS4/Cloud-Web-Services-Guide-DWS4.pdf#page=33) |
| [Get Template Sample Data](actions/get-template-sample-data.md) | `POST /getSampleData` | [docs](https://resources.docmosis.com/Documentation/Cloud/DWS4/Cloud-Web-Services-Guide-DWS4.pdf#page=58) |
| [Get Template Structure](actions/get-template-structure.md) | `POST /getTemplateStructure` | [docs](https://resources.docmosis.com/Documentation/Cloud/DWS4/Cloud-Web-Services-Guide-DWS4.pdf#page=34) |
| [Get Upload Template Batch Status](actions/get-upload-template-batch-status.md) | `POST /uploadTemplateBatchStatus` | [docs](https://resources.docmosis.com/Documentation/Cloud/DWS4/Cloud-Web-Services-Guide-DWS4.pdf#page=44) |
| [List Images](actions/list-images.md) | `POST /listImages` | [docs](https://resources.docmosis.com/Documentation/Cloud/DWS4/Cloud-Web-Services-Guide-DWS4.pdf#page=49) |
| [List Templates](actions/list-templates.md) | `POST /listTemplates` | [docs](https://resources.docmosis.com/Documentation/Cloud/DWS4/Cloud-Web-Services-Guide-DWS4.pdf#page=37) |
| [Ping](actions/ping.md) | `GET /ping` | [docs](https://resources.docmosis.com/Documentation/Cloud/DWS4/Cloud-Web-Services-Guide-DWS4.pdf#page=61) |
| [Render Documents](actions/render-documents.md) | `POST /render` | [docs](https://resources.docmosis.com/Documentation/Cloud/DWS4/Cloud-Web-Services-Guide-DWS4.pdf#page=15) |
| [Upload Image](actions/upload-image.md) | `POST /uploadImage` | [docs](https://resources.docmosis.com/Documentation/Cloud/DWS4/Cloud-Web-Services-Guide-DWS4.pdf#page=47) |
| [Upload Template](actions/upload-template.md) | `POST /uploadTemplate` | [docs](https://resources.docmosis.com/Documentation/Cloud/DWS4/Cloud-Web-Services-Guide-DWS4.pdf#page=29) |
| [Upload Template Batch](actions/upload-template-batch.md) | `POST /uploadTemplateBatch` | [docs](https://resources.docmosis.com/Documentation/Cloud/DWS4/Cloud-Web-Services-Guide-DWS4.pdf#page=40) |
