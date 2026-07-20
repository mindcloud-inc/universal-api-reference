# Search Contacts with Bexio

Finds contacts in Bexio by search criteria.

## Endpoint

- **Method:** `POST`
- **Path:** `/2.0/contact/search`
- **Base URL:** `https://api.bexio.com`
- **Official documentation:** [Search Contacts](https://docs.bexio.com/#tag/Contacts/operation/v2SearchContact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input[]` | body | `array<object>` | no | Array of contact search clauses sent as the request body. |
| `input[].field` | body | `list<string>` | yes | Contact field to search over. Accepted values: `address`, `city`, `contact_group_ids`, `contact_type_id`, `country_id`, `fax`, `id`, `mail`, `mail_second`, `name_1`, `name_2`, `nr`, `phone_fixed`, `phone_mobile`, `postcode`, `updated_at`, `user_id`. |
| `input[].criteria` | body | `list<string>` | no | Comparison operator for the search clause. Defaults to like. Accepted values: `!=`, `<`, `<=`, `=`, `>`, `>=`, `equal`, `greater_equal`, `greater_than`, `in`, `is_null`, `less_equal`, `less_than`, `like`, `not_equal`, `not_in`, `not_like`, `not_null`. |
| `input[].value` | body | `string` | yes | Value to search for. |
