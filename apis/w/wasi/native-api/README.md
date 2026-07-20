# Wasi: Native API Reference

A consolidated summary of Wasi's API configuration and 25 documented operations, with links to official documentation.

- **Official docs:** https://api.wasi.co/docs/en/guide/
- **API base URL:** `https://api.wasi.co/v1`

## Authentication

### Wasi Credentials

Use your Wasi company ID and Wasi token exactly as provided by Wasi API settings.

### Credentials

- **Company ID:** `company_id` · required · Your Wasi company identifier.
- **Wasi Token:** `wasi_token` · required · Your Wasi API token.

[Official authentication documentation](https://api.wasi.co/docs/en/guide/getting-started.html)

## API conventions

Responses from this API use JSON.

## Pagination

Use `take` in the query string to set the page size (default 10; maximum 100). Use `skip` in the query string as the record offset; numbering starts at 0.

## Sorting

Set the sort field with `order_by` in the query string. Set the direction separately with `order`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (25 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Change Property Label](actions/change-property-label.md) | `POST /property/change-label/:id_property` | [docs](https://api.wasi.co/docs/en/guide/properties.html) |
| [Create Client](actions/create-client.md) | `POST /client/add` | [docs](https://api.wasi.co/docs/en/guide/clients.html) |
| [Create Property](actions/create-property.md) | `POST /property/add` | [docs](https://api.wasi.co/docs/en/guide/properties.html) |
| [Get Client](actions/get-client.md) | `GET /client/get/:id_client` | [docs](https://api.wasi.co/docs/en/guide/clients.html) |
| [Get Property](actions/get-property.md) | `GET /property/get/:id_property` | [docs](https://api.wasi.co/docs/en/guide/properties.html) |
| [Get Property Commission](actions/get-property-commission.md) | `GET /property/get-commission/:id_property` | [docs](https://api.wasi.co/docs/en/guide/properties.html) |
| [Link Client To Property](actions/link-client-to-property.md) | `POST /client/:id_client/add-property/:id_property` | [docs](https://api.wasi.co/docs/en/guide/clients.html) |
| [List Cities With Property](actions/list-cities-with-property.md) | `GET /location/cities-with-property` | [docs](https://api.wasi.co/docs/en/guide/cities.html) |
| [List Client Properties](actions/list-client-properties.md) | `GET /client/properties/:id_client` | [docs](https://api.wasi.co/docs/en/guide/clients.html) |
| [List Client Types](actions/list-client-types.md) | `GET /client-type/all` | [docs](https://api.wasi.co/docs/en/guide/clients.html) |
| [List Clients](actions/list-clients.md) | `GET /client/search` | [docs](https://api.wasi.co/docs/en/guide/clients.html) |
| [List Countries](actions/list-countries.md) | `GET /location/all-countries` | [docs](https://api.wasi.co/docs/en/guide/countries.html) |
| [List Currencies](actions/list-currencies.md) | `GET /property/currency-all` | [docs](https://api.wasi.co/docs/en/guide/currencies.html) |
| [List Properties](actions/list-properties.md) | `GET /property/search` | [docs](https://api.wasi.co/docs/en/guide/properties.html) |
| [List Property Clients](actions/list-property-clients.md) | `GET /property/clients/:id_property` | [docs](https://api.wasi.co/docs/en/guide/properties.html) |
| [List Property Types](actions/list-property-types.md) | `GET /property-type/all` | [docs](https://api.wasi.co/docs/en/guide/properties.html) |
| [Remove Client Property Link](actions/remove-client-property-link.md) | `POST /client/:id_client/remove-property/:id_property` | [docs](https://api.wasi.co/docs/en/guide/clients.html) |
| [Remove Property Image](actions/remove-property-image.md) | `POST /property/remove-image/:id_property` | [docs](https://api.wasi.co/docs/en/guide/properties.html) |
| [Remove Property Label](actions/remove-property-label.md) | `POST /property/remove-label/:id_property` | [docs](https://api.wasi.co/docs/en/guide/properties.html) |
| [Send Property To Portals](actions/send-property-to-portals.md) | `GET /portal/send-property/:id_property` | [docs](https://api.wasi.co/docs/en/guide/properties.html) |
| [Update Client](actions/update-client.md) | `POST /client/update/:id_client` | [docs](https://api.wasi.co/docs/en/guide/clients.html) |
| [Update Client Property Link](actions/update-client-property-link.md) | `POST /client/:id_client/update-property/:id_property` | [docs](https://api.wasi.co/docs/en/guide/clients.html) |
| [Update Property](actions/update-property.md) | `POST /property/update/:id_property` | [docs](https://api.wasi.co/docs/en/guide/properties.html) |
| [Update Property Image](actions/update-property-image.md) | `POST /gallery/image/update-data/:id_image` | [docs](https://api.wasi.co/docs/en/guide/properties.html) |
| [Upload Property Image](actions/upload-property-image.md) | `POST /property/upload-image/:id_property` | [docs](https://api.wasi.co/docs/en/guide/properties.html) |
