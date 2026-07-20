# <img src="https://images.mindcloud.co/apps/icons/docuwriter_1775489524733.png" alt="DocuWriter.ai logo" width="28" height="28"> DocuWriter.ai: Universal API

AI documentation platform for generating code docs, tests, UML diagrams, API references, and managing documentation spaces with repository sync.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/docuWriterai/latest
- **Category:** Productivity / Knowledge Management
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.docuwriter.ai/
- **Vendor API docs:** https://docs.docuwriter.ai/docuwriterai-api-docs/92073

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Spaces](actions/list-spaces.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docuWriterai/latest/actions/list-spaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Comment

| Action | Method | Description |
| --- | --- | --- |
| [Generate Code Comments](actions/generate-code-comments.md) | POST |  |

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Create Space Document](actions/create-space-document.md) | POST |  |
| [Delete Space Document](actions/delete-space-document.md) | DELETE |  |
| [Get Space Document](actions/get-space-document.md) | GET |  |
| [List Space Documents](actions/list-space-documents.md) | GET |  |
| [Update Space Document](actions/update-space-document.md) | PUT |  |

### Documentation

| Action | Method | Description |
| --- | --- | --- |
| [Generate Code Documentation](actions/generate-code-documentation.md) | POST |  |
| [Generate Multi-File Documentation](actions/generate-multi-file-documentation.md) | POST |  |

### Generation

| Action | Method | Description |
| --- | --- | --- |
| [Get Generation](actions/get-generation.md) | GET |  |
| [List Generations](actions/list-generations.md) | GET |  |
| [List My Generations](actions/list-my-generations.md) | GET |  |

### Optimization

| Action | Method | Description |
| --- | --- | --- |
| [Generate Code Optimization](actions/generate-code-optimization.md) | POST |  |

### Repository

| Action | Method | Description |
| --- | --- | --- |
| [List Repositories](actions/list-repositories.md) | GET |  |

### Space

| Action | Method | Description |
| --- | --- | --- |
| [Create Space](actions/create-space.md) | POST |  |
| [Search Space](actions/search-space.md) | GET |  |

### Test

| Action | Method | Description |
| --- | --- | --- |
| [Generate Code Tests](actions/generate-code-tests.md) | POST |  |

### Uml

| Action | Method | Description |
| --- | --- | --- |
| [Generate UML Diagram](actions/generate-uml-diagram.md) | POST |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET |  |
| [Get User Info](actions/get-user-info.md) | GET |  |

### Workspaces

| Action | Method | Description |
| --- | --- | --- |
| [List Spaces](actions/list-spaces.md) | GET |  |

