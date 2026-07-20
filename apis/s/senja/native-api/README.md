# Senja: Native API Reference

A consolidated summary of Senja's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://support.senja.io/articles/rest-api-wbnz4
- **API base URL:** `https://api.senja.io/v1`

## Authentication

### API Key

Connect with a Senja API key generated from your project settings.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://support.senja.io/articles/where-do-i-find-my-api-key-r54b6)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `limit` in the query string to set the page size (maximum 100). Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `sort` in the query string. Set the direction separately with `order`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Testimonial](actions/create-testimonial.md) | `POST /testimonials` | [docs](https://support.senja.io/articles/rest-api-wbnz4#create-a-testimonial) |
| [Get Testimonial](actions/get-testimonial.md) | `GET /testimonials/:id` | [docs](https://support.senja.io/articles/rest-api-wbnz4) |
| [List Testimonials](actions/list-testimonials.md) | `GET /testimonials` | [docs](https://support.senja.io/articles/rest-api-wbnz4#list-testimonials-in-your-senja-project) |
