# List Internal Accounts with Modern Treasury

Retrieves internal accounts from Modern Treasury.

## Endpoint

- **Method:** `GET`
- **Path:** `/internal_accounts`
- **Base URL:** `https://app.moderntreasury.com/api`
- **Official documentation:** [List Internal Accounts](https://docs.moderntreasury.com/platform/reference/list-internal-accounts)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `currency` | query | `string` | no | Only return internal accounts with this currency. |
| `counterparty_id` | query | `string` | no | Only return internal accounts associated with this counterparty. |
| `legal_entity_id` | query | `string` | no | Only return internal accounts associated with this legal entity. |
| `payment_type` | query | `string` | no | Only return internal accounts that can make this type of payment. |
| `payment_direction` | query | `list<string>` | no | Only return internal accounts that can originate payments with this direction. Accepted values: `0`, `1`. |
| `status` | query | `list<string>` | no | Only return internal accounts with this status. Accepted values: `0`, `1`, `2`, `3`, `4`. |
| `external_id` | query | `string` | no | Only return internal accounts with this user-defined external ID. |
| `metadata` | query | `string` | no | Metadata filter using Modern Treasury's metadata query format. |
