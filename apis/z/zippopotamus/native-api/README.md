# Zippopotamus: Native API Reference

A consolidated summary of Zippopotamus's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://docs.zippopotam.us/docs/v1/
- **API base URL:** `https://api.zippopotam.us`

## Authentication

### No authentication

Zippopotam.us public API requests do not require credentials.

This API does not require request authentication.

[Official authentication documentation](https://docs.zippopotam.us/)

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Nearby Places by Postal Code](actions/list-nearby-places-by-postal-code.md) | `GET /nearby/{{country}}/{{postalcode}}` | [docs](https://docs.zippopotam.us/docs/v1/#places-near-postal-code) |
| [List Postal Codes by Place](actions/list-postal-codes-by-place.md) | `GET /{{country}}/{{state}}/{{place}}` | [docs](https://docs.zippopotam.us/docs/v1/#postal-codes-by-place) |
| [Look Up Places by Postal Code](actions/lookup-places-by-postal-code.md) | `GET /{{country}}/{{postalcode}}` | [docs](https://docs.zippopotam.us/docs/v1/#places-by-postal-code) |
