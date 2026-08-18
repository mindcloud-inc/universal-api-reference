# Search Revenue Transactions with BlackBaud

## Endpoint

- **Method:** `GET`
- **Path:** `alt-revmg/revenuetransactions/search`
- **Base URL:** `https://api.sky.blackbaud.com/`
- **Official documentation:** [Search Revenue Transactions](https://developer.blackbaud.com/skyapi/products/altru/revenue)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `key_name` | query | `string` | no | Last, organization, or group name. |
| `first_name` | query | `string` | no | First name. |
| `lookup_id` | query | `string` | no | Constituent lookup ID. |
| `payment_method` | query | `string` | no | Payment method. |
| `transaction_type` | query | `string` | no | Transaction type. |
| `revenue_type` | query | `string` | no | Revenue type. |
| `transaction_amount` | query | `number` | no | Transaction amount. |
| `transaction_date` | query | `date` | no | Start date in RFC 3339 full-date format. |
| `batch_number` | query | `string` | no | Batch number. |
| `include_inactive` | query | `boolean` | no | Include inactive constituents. |
| `include_deceased` | query | `boolean` | no | Include deceased constituents. |
| `check_nickname` | query | `boolean` | no | Check constituent nicknames. |
| `check_aliases` | query | `boolean` | no | Check constituent aliases. |
| `exact_match_only` | query | `boolean` | no | Match all criteria exactly. |
| `receipt_number` | query | `string` | no | Receipt number. |
| `check_alternate_lookup_ids` | query | `boolean` | no | Check alternate constituent lookup IDs. |
| `revenue_lookup_id` | query | `string` | no | Revenue ID. |
| `address_block` | query | `string` | no | Address. |
| `city` | query | `string` | no | City. |
| `state` | query | `string` | no | State identifier. |
| `post_code` | query | `string` | no | ZIP or postal code. |
| `country` | query | `string` | no | Country identifier. |
| `only_primary_address` | query | `boolean` | no | Search only primary addresses. |
| `phone_number` | query | `string` | no | Phone number. |
| `email_address` | query | `string` | no | Email address. |
| `include_individuals` | query | `boolean` | no | Include individuals. |
| `include_organizations` | query | `boolean` | no | Include organizations. |
| `include_groups` | query | `boolean` | no | Include groups and households. |
| `appeal` | query | `string` | no | Appeal. |
| `channel` | query | `string` | no | Inbound channel code. |
| `designation` | query | `string` | no | Designation. |
| `transaction_end_date` | query | `date` | no | End date in RFC 3339 full-date format. |
| `include_transactions_with_no_constituent` | query | `boolean` | no | Include transactions with no constituent. |
