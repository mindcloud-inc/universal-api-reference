# Rebrickable: Native API Reference

A consolidated summary of Rebrickable's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://rebrickable.com/api/v3/docs/?key=xxxxxxxxxx
- **OpenAPI specification:** https://rebrickable.com/api/v3/swagger/?format=openapi
- **API base URL:** `https://rebrickable.com/api/v3`

## Authentication

### API Key

Authenticate Rebrickable API requests with an API key. Rebrickable requires the Authorization header value to use the format `key <api_key>`.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://rebrickable.com/api/v3/docs/?key=xxxxxxxxxx)

## API conventions

The next-page cursor is read from `next`.

## Pagination

Use `page_size` in the query string to set the page size (default 100; accepted range 1–1000). Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `ordering` in the query string. Prefix the field name to select its direction. Multiple sort fields can be combined.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Badge](actions/get-badge.md) | `GET /users/badges/:id/` | [docs](https://rebrickable.com/api/v3/docs/?key=xxxxxxxxxx) |
| [Get Color](actions/get-color.md) | `GET /lego/colors/:id/` | [docs](https://rebrickable.com/api/v3/docs/?key=xxxxxxxxxx) |
| [Get Element](actions/get-element.md) | `GET /lego/elements/:element_id/` | [docs](https://rebrickable.com/api/v3/docs/?key=xxxxxxxxxx) |
| [Get Minifig](actions/get-minifig.md) | `GET /lego/minifigs/:set_num/` | [docs](https://rebrickable.com/api/v3/docs/?key=xxxxxxxxxx) |
| [Get Part](actions/get-part.md) | `GET /lego/parts/:part_num/` | [docs](https://rebrickable.com/api/v3/docs/?key=xxxxxxxxxx) |
| [Get Part Category](actions/get-part-category.md) | `GET /lego/part_categories/:id/` | [docs](https://rebrickable.com/api/v3/docs/?key=xxxxxxxxxx) |
| [Get Part Color](actions/get-part-color.md) | `GET /lego/parts/:part_num/colors/:color_id/` | [docs](https://rebrickable.com/api/v3/docs/?key=xxxxxxxxxx) |
| [Get Set](actions/get-set.md) | `GET /lego/sets/:set_num/` | [docs](https://rebrickable.com/api/v3/docs/?key=xxxxxxxxxx) |
| [Get Theme](actions/get-theme.md) | `GET /lego/themes/:id/` | [docs](https://rebrickable.com/api/v3/docs/?key=xxxxxxxxxx) |
| [List Alternate Builds for Set](actions/list-alternate-builds-for-set.md) | `GET /lego/sets/:set_num/alternates/` | [docs](https://rebrickable.com/api/v3/docs/?key=xxxxxxxxxx) |
| [List Badges](actions/list-badges.md) | `GET /users/badges/` | [docs](https://rebrickable.com/api/v3/docs/?key=xxxxxxxxxx) |
| [List Colors](actions/list-colors.md) | `GET /lego/colors/` | [docs](https://rebrickable.com/api/v3/docs/?key=xxxxxxxxxx) |
| [List Minifig Parts](actions/list-minifig-parts.md) | `GET /lego/minifigs/:set_num/parts/` | [docs](https://rebrickable.com/api/v3/docs/?key=xxxxxxxxxx) |
| [List Minifigs](actions/list-minifigs.md) | `GET /lego/minifigs/` | [docs](https://rebrickable.com/api/v3/docs/?key=xxxxxxxxxx) |
| [List Part Categories](actions/list-part-categories.md) | `GET /lego/part_categories/` | [docs](https://rebrickable.com/api/v3/docs/?key=xxxxxxxxxx) |
| [List Part Colors](actions/list-part-colors.md) | `GET /lego/parts/:part_num/colors/` | [docs](https://rebrickable.com/api/v3/docs/?key=xxxxxxxxxx) |
| [List Parts](actions/list-parts.md) | `GET /lego/parts/` | [docs](https://rebrickable.com/api/v3/docs/?key=xxxxxxxxxx) |
| [List Set Minifigs](actions/list-set-minifigs.md) | `GET /lego/sets/:set_num/minifigs/` | [docs](https://rebrickable.com/api/v3/docs/?key=xxxxxxxxxx) |
| [List Set Parts](actions/list-set-parts.md) | `GET /lego/sets/:set_num/parts/` | [docs](https://rebrickable.com/api/v3/docs/?key=xxxxxxxxxx) |
| [List Set Subsets](actions/list-set-subsets.md) | `GET /lego/sets/:set_num/sets/` | [docs](https://rebrickable.com/api/v3/docs/?key=xxxxxxxxxx) |
| [List Sets](actions/list-sets.md) | `GET /lego/sets/` | [docs](https://rebrickable.com/api/v3/docs/?key=xxxxxxxxxx) |
| [List Sets Containing Minifig](actions/list-sets-containing-minifig.md) | `GET /lego/minifigs/:set_num/sets/` | [docs](https://rebrickable.com/api/v3/docs/?key=xxxxxxxxxx) |
| [List Sets Containing Part Color](actions/list-sets-containing-part-color.md) | `GET /lego/parts/:part_num/colors/:color_id/sets/` | [docs](https://rebrickable.com/api/v3/docs/?key=xxxxxxxxxx) |
| [List Themes](actions/list-themes.md) | `GET /lego/themes/` | [docs](https://rebrickable.com/api/v3/docs/?key=xxxxxxxxxx) |
