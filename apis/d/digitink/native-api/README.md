# Digit.ink: Native API Reference

A consolidated summary of Digit.ink's API configuration and 14 documented operations, with links to official documentation.

- **Official docs:** https://app.digit.ink/api/v1/
- **OpenAPI specification:** https://app.digit.ink/api/v1/js/swagger.json
- **API base URL:** `https://app.digit.ink/api/v1`

## Authentication

### API Key

Authenticate Digit.ink requests with an API key and issuer public key.

### Credentials

- **API Key:** `apiKey` · required
- **Issuer Public Key:** `issuerPubkey` · required · Issuer public key used to populate the shared issuer-pubkey request header.

Send these headers with each API request:

```http
api-key: <apiKey>
issuer-pubkey: <issuerPubkey>
```

[Official authentication documentation](https://app.digit.ink/api/v1/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (14 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Batch To Stack](actions/add-batch-to-stack.md) | `POST /stacks/:stackUuid` | [docs](https://app.digit.ink/api/v1/classic-docs) |
| [Create Stack](actions/create-stack.md) | `POST /stacks` | [docs](https://app.digit.ink/api/v1/classic-docs) |
| [Delete Stacks](actions/delete-stacks.md) | `DELETE /stacks` | [docs](https://app.digit.ink/api/v1/classic-docs) |
| [Get Batch](actions/get-batch.md) | `GET /batches/:batchUuid` | [docs](https://app.digit.ink/api/v1/classic-docs) |
| [Get Credential](actions/get-credential.md) | `GET /credentials/:credentialUuid` | [docs](https://app.digit.ink/api/v1/classic-docs) |
| [Get Credential Stack](actions/get-credential-stack.md) | `GET /credentials/:credentialUuid/stack` | [docs](https://app.digit.ink/api/v1/classic-docs) |
| [Get Issuer Profile](actions/get-issuer-profile.md) | `GET /issuers/:issuerPubkey` | [docs](https://app.digit.ink/api/v1/classic-docs) |
| [Get Stack](actions/get-stack.md) | `GET /stacks/:stackUuid` | [docs](https://app.digit.ink/api/v1/classic-docs) |
| [Get Template](actions/get-template.md) | `GET /templates/:templateUuid` | [docs](https://app.digit.ink/api/v1/classic-docs) |
| [Issue Credentials](actions/issue-credentials.md) | `POST /credentials` | [docs](https://app.digit.ink/api/v1/classic-docs) |
| [List Batches](actions/list-batches.md) | `GET /batches` | [docs](https://app.digit.ink/api/v1/classic-docs) |
| [List Credentials](actions/list-credentials.md) | `GET /credentials` | [docs](https://app.digit.ink/api/v1/classic-docs) |
| [List Stacks](actions/list-stacks.md) | `GET /stacks` | [docs](https://app.digit.ink/api/v1/classic-docs) |
| [List Templates](actions/list-templates.md) | `GET /templates` | [docs](https://app.digit.ink/api/v1/classic-docs) |
