# Direct Mail Manager: Native API Reference

A consolidated summary of Direct Mail Manager's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://apidocs.directmailmanager.com/
- **API base URL:** `https://api.directmailmanager.com/api`

## Authentication

### API Key

Use a Direct Mail Manager API key from the account settings API Keys page.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://apidocs.directmailmanager.com/docs/dmm-v3-api)

## API conventions

The total page count is read from `meta.last_page`. The current page number is read from `meta.current_page`.

## Pagination

Use `page[number]` in the query string to choose the page; numbering starts at 1.

## Filtering

Send filters in the query string.

## Sorting

Set the sort field with `sort` in the query string. Only one sort field is accepted.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Attach Address To Mailing List](actions/attach-address-to-mailing-list.md) | `POST /addresses/:adr_id/attach` | [docs](https://apidocs.directmailmanager.com/#tag/Addresses/operation/attach-an-address) |
| [Create Address](actions/create-address.md) | `POST /addresses` | [docs](https://apidocs.directmailmanager.com/#tag/Addresses/operation/create-an-address) |
| [Create Company Address](actions/create-company-address.md) | `POST /company-addresses` | [docs](https://apidocs.directmailmanager.com/#tag/Company-Addresses/operation/create_company_address) |
| [Create Custom Field](actions/create-custom-field.md) | `POST /custom-fields` | [docs](https://apidocs.directmailmanager.com/#tag/Custom-Fields/operation/create_custom_field) |
| [Create Letter](actions/create-letter.md) | `POST /letters` | [docs](https://apidocs.directmailmanager.com/#tag/Letters/operation/create_letter) |
| [Create Mailing List](actions/create-mailing-list.md) | `POST /mailing-lists` | [docs](https://apidocs.directmailmanager.com/#tag/Mailing-Lists/operation/create_mailing_list) |
| [Create Postcard](actions/create-postcard.md) | `POST /postcards` | [docs](https://apidocs.directmailmanager.com/#tag/Postcards/operation/create_postcard) |
| [Create Segment](actions/create-segment.md) | `POST /segments` | [docs](https://apidocs.directmailmanager.com/#tag/Segments/operation/create_segment) |
| [Delete Mailing List](actions/delete-mailing-list.md) | `DELETE /mailing-lists/:mlg_lst_id` | [docs](https://apidocs.directmailmanager.com/#tag/Mailing-Lists/operation/delete-mailing-list) |
| [Detach Address From Mailing List](actions/detach-address-from-mailing-list.md) | `POST /addresses/:adr_id/detach` | [docs](https://apidocs.directmailmanager.com/#tag/Addresses/operation/detach-an-address) |
| [Get Custom Field](actions/get-custom-field.md) | `GET /custom-fields/:cfld_id` | [docs](https://apidocs.directmailmanager.com/#tag/Custom-Fields/operation/get_custom_field) |
| [Get Mailing List](actions/get-mailing-list.md) | `GET /mailing-lists/:mlg_lst_id` | [docs](https://apidocs.directmailmanager.com/#tag/Mailing-Lists/operation/get_mailing_list) |
| [Get Segment](actions/get-segment.md) | `GET /segments/:sgm_id` | [docs](https://apidocs.directmailmanager.com/#tag/Segments/operation/get_segment) |
| [Import Addresses](actions/import-addresses.md) | `POST /addresses/import` | [docs](https://apidocs.directmailmanager.com/#tag/Addresses/operation/address-import) |
| [List Addresses](actions/list-addresses.md) | `GET /addresses` | [docs](https://apidocs.directmailmanager.com/#tag/Addresses/operation/list_addresses) |
| [List Company Addresses](actions/list-company-addresses.md) | `GET /company-addresses` | [docs](https://apidocs.directmailmanager.com/#tag/Company-Addresses/operation/list_company_addresses) |
| [List Custom Fields](actions/list-custom-fields.md) | `GET /custom-fields` | [docs](https://apidocs.directmailmanager.com/#tag/Custom-Fields/operation/list_custom_fields) |
| [List Letters](actions/list-letters.md) | `GET /letters` | [docs](https://apidocs.directmailmanager.com/#tag/Letters/operation/list_letters) |
| [List Mailing List Addresses](actions/list-mailing-list-addresses.md) | `GET /mailing-lists/:mlg_lst_id/addresses` | [docs](https://apidocs.directmailmanager.com/#tag/Mailing-Lists/operation/list_mailing_list_addresses) |
| [List Mailing Lists](actions/list-mailing-lists.md) | `GET /mailing-lists` | [docs](https://apidocs.directmailmanager.com/#tag/Mailing-Lists/operation/list_mailing_list) |
| [List Postcards](actions/list-postcards.md) | `GET /postcards` | [docs](https://apidocs.directmailmanager.com/#tag/Postcards/operation/list_postcards) |
| [List Segment Addresses](actions/list-segment-addresses.md) | `GET /segments/:sgm_id/addresses` | [docs](https://apidocs.directmailmanager.com/#tag/Segments/operation/list_segmented_addresses) |
| [List Segments](actions/list-segments.md) | `GET /segments` | [docs](https://apidocs.directmailmanager.com/#tag/Segments/operation/list_segments) |
| [Retrieve Address](actions/retrieve-address.md) | `GET /addresses/:adr_id` | [docs](https://apidocs.directmailmanager.com/#tag/Addresses/operation/retrieve-an-address) |
| [Suppress Address](actions/suppress-address.md) | `PATCH /addresses/:adr_id/suppress` | [docs](https://apidocs.directmailmanager.com/#tag/Addresses/operation/suppress-an-address) |
| [Unsuppress Address](actions/unsuppress-address.md) | `PATCH /addresses/:adr_id/un-suppress` | [docs](https://apidocs.directmailmanager.com/#tag/Addresses/operation/unsuppress-an-address) |
| [Update Address](actions/update-address.md) | `PUT /addresses/:adr_id` | [docs](https://apidocs.directmailmanager.com/#tag/Addresses/operation/update-an-address) |
| [Update Custom Field](actions/update-custom-field.md) | `PUT /custom-fields/:cfld_id` | [docs](https://apidocs.directmailmanager.com/#tag/Custom-Fields/operation/update_custom_field) |
| [Update Mailing List](actions/update-mailing-list.md) | `PUT /mailing-lists/:mlg_lst_id` | [docs](https://apidocs.directmailmanager.com/#tag/Mailing-Lists/operation/update-mailing-list) |
| [Update Segment](actions/update-segment.md) | `PUT /segments/:sgm_id` | [docs](https://apidocs.directmailmanager.com/#tag/Segments/operation/update_segment) |
