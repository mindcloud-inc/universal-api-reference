# gotoHuman: Native API Reference

A consolidated summary of gotoHuman's API configuration and 7 documented operations, with links to official documentation.

- **Official docs:** https://docs.gotohuman.com/
- **API base URL:** `https://api.gotohuman.com`

## Authentication

### API Key

Connect with your gotoHuman API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://docs.gotohuman.com/send-requests)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (7 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Review Request](actions/create-review-request.md) | `POST /requestReview` | [docs](https://docs.gotohuman.com/send-requests) |
| [Fetch Responses](actions/fetch-responses.md) | `GET /fetchResponses` | [docs](https://docs.gotohuman.com/agent-memory) |
| [Get Form Schema](actions/get-form-schema.md) | `GET /fetchSchemaForFormFields` | [docs](https://github.com/gotohuman/gotohuman-mcp-server/blob/main/README.md) |
| [List Review Forms](actions/list-review-forms.md) | `GET /fetchReviewForms` | [docs](https://github.com/gotohuman/gotohuman-mcp-server/blob/main/README.md) |
| [Query Responses](actions/query-responses.md) | `GET /queryResponses` | [docs](https://docs.gotohuman.com/training-data) |
| [Update Review Request](actions/update-review-request.md) | `POST /requestReview` | [docs](https://docs.gotohuman.com/retries) |
| [Upload Files](actions/upload-files.md) | `POST /uploadFiles` | [docs](https://docs.gotohuman.com/send-requests) |
