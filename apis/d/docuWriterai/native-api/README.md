# DocuWriter.ai: Native API Reference

A consolidated summary of DocuWriter.ai's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://docs.docuwriter.ai/docuwriterai-api-docs/92073
- **API base URL:** `https://app.docuwriter.ai`

## Authentication

### Bearer Token

Personal access token used as a Bearer token for DocuWriter.ai REST API requests.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.docuwriter.ai/docuwriterai-api-docs/92073)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON. Response data is read from `data`.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Space](actions/create-space.md) | `POST /api/spaces` | [docs](https://docs.docuwriter.ai/docuwriterai-api-docs/358013) |
| [Create Space Document](actions/create-space-document.md) | `POST /api/spaces/{{space}}/documents` | [docs](https://docs.docuwriter.ai/docuwriterai-api-docs/92056) |
| [Delete Space Document](actions/delete-space-document.md) | `DELETE /api/spaces/{{space}}/documents/{{spaceMenuItem}}` | [docs](https://docs.docuwriter.ai/docuwriterai-api-docs/92057) |
| [Generate Code Comments](actions/generate-code-comments.md) | `POST /api/generate-code-comments` | [docs](https://docs.docuwriter.ai/docuwriterai-api-docs/92067) |
| [Generate Code Documentation](actions/generate-code-documentation.md) | `POST /api/generate-code-documentation` | [docs](https://docs.docuwriter.ai/docuwriterai-api-docs/92064) |
| [Generate Code Optimization](actions/generate-code-optimization.md) | `POST /api/generate-code-optimization` | [docs](https://docs.docuwriter.ai/docuwriterai-api-docs/92062) |
| [Generate Code Tests](actions/generate-code-tests.md) | `POST /api/generate-code-tests` | [docs](https://docs.docuwriter.ai/docuwriterai-api-docs/92068) |
| [Generate Multi-File Documentation](actions/generate-multi-file-documentation.md) | `POST /api/generate-multi-file-documentation` | [docs](https://docs.docuwriter.ai/docuwriterai-api-docs/92069) |
| [Generate UML Diagram](actions/generate-uml-diagram.md) | `POST /api/generate-uml-diagram` | [docs](https://docs.docuwriter.ai/docuwriterai-api-docs/92070) |
| [Get Current User](actions/get-current-user.md) | `POST /api/user` | [docs](https://docs.docuwriter.ai/docuwriterai-api-docs/92052) |
| [Get Generation](actions/get-generation.md) | `GET /api/generations/{{id}}` | [docs](https://docs.docuwriter.ai/docuwriterai-api-docs/92066) |
| [Get Space Document](actions/get-space-document.md) | `GET /api/spaces/{{space}}/documents/{{spaceMenuItem}}` | [docs](https://docs.docuwriter.ai/docuwriterai-api-docs/92054) |
| [Get User Info](actions/get-user-info.md) | `GET /api/user-info` | [docs](https://docs.docuwriter.ai/docuwriterai-api-docs/92053) |
| [List Generations](actions/list-generations.md) | `GET /api/generations` | [docs](https://docs.docuwriter.ai/docuwriterai-api-docs/92060) |
| [List My Generations](actions/list-my-generations.md) | `POST /api/my-generations` | [docs](https://docs.docuwriter.ai/docuwriterai-api-docs/92071) |
| [List Repositories](actions/list-repositories.md) | `GET /api/repositories` | [docs](https://docs.docuwriter.ai/docuwriterai-api-docs/92075) |
| [List Space Documents](actions/list-space-documents.md) | `GET /api/spaces/{{space_id}}/documents` | [docs](https://docs.docuwriter.ai/docuwriterai-api-docs/118761) |
| [List Spaces](actions/list-spaces.md) | `GET /api/spaces` | [docs](https://docs.docuwriter.ai/docuwriterai-api-docs/92058) |
| [Search Space](actions/search-space.md) | `POST /api/spaces/{{space}}/search` | [docs](https://docs.docuwriter.ai/docuwriterai-api-docs/92055) |
| [Update Space Document](actions/update-space-document.md) | `PUT /api/spaces/{{space}}/documents/{{spaceMenuItem}}` | [docs](https://docs.docuwriter.ai/docuwriterai-api-docs/92059) |
