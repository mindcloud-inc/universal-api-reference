# NYC Squirrel Census: Native API Reference

A consolidated summary of NYC Squirrel Census's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://dev.socrata.com/foundry/data.cityofnewyork.us/vfnx-vebw
- **API base URL:** `https://data.cityofnewyork.us`

## Authentication

### No authentication

This public NYC Open Data/Socrata resource can be read without credentials.

This API does not require request authentication.

[Official authentication documentation](https://dev.socrata.com/foundry/data.cityofnewyork.us/vfnx-vebw)

## Pagination

Use `$limit` in the query string to set the page size (default 1000; accepted range 1–50000). Use `$offset` in the query string as the record offset; numbering starts at 0.

## Sorting

Set the sort field with `$order` in the query string. Only one sort field is accepted.

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List squirrel sightings](actions/list-squirrel-sightings.md) | `GET /resource/vfnx-vebw.json` | [docs](https://dev.socrata.com/foundry/data.cityofnewyork.us/vfnx-vebw) |
