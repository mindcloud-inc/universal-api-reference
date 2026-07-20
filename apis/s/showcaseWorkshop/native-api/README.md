# Showcase Workshop: Native API Reference

A consolidated summary of Showcase Workshop's API configuration and 4 documented operations, with links to official documentation.

- **Official docs:** https://github.com/ShowcaseSoftwareLtd/showcase-workshop-apis
- **API base URL:** `https://app.showcaseworkshop.com/api/v1`

## Authentication

### Developer Key

Authenticate requests with a Showcase Workshop developer key passed as the `access_token` query parameter.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://github.com/ShowcaseSoftwareLtd/showcase-workshop-apis/blob/main/rest-api/README.md)

## API conventions

Responses from this API use JSON.

## Pagination

Use `page` in the query string to choose the page; numbering starts at 1.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (4 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Data](actions/add-data.md) | `POST /data/` | [docs](https://github.com/ShowcaseSoftwareLtd/showcase-workshop-apis/blob/main/rest-api/README.md#add-data) |
| [Delete Data](actions/delete-data.md) | `DELETE /data/{guid}` | [docs](https://github.com/ShowcaseSoftwareLtd/showcase-workshop-apis/blob/main/rest-api/README.md#delete) |
| [Get Data](actions/get-data.md) | `GET /data/{guid}` | [docs](https://github.com/ShowcaseSoftwareLtd/showcase-workshop-apis/blob/main/rest-api/README.md#get-data) |
| [List Data](actions/list-data.md) | `GET /data/` | [docs](https://github.com/ShowcaseSoftwareLtd/showcase-workshop-apis/blob/main/rest-api/README.md#list-data) |
