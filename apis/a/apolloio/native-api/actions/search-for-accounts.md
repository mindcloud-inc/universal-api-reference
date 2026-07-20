# Search for Accounts with Apollo

Finds accounts in your Apollo account.

## Endpoint

- **Method:** `POST`
- **Path:** `v1/accounts/search`
- **Base URL:** `https://app.apollo.io/api`
- **Official documentation:** [Search for Accounts](https://docs.apollo.io/reference/search-for-accounts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q_organization_name` | body | `string` | no | Add keywords to narrow the search of the accounts in your team's Apollo account. Keywords should directly match at least part of an account's name. For example, searching the keyword `marketing` might return the result `NY Marketing Unlimited`, but not `NY Market Analysts`. This parameter only searches account names, not other account fields. Examples: `apollo`; `microsoft`; `marketing` |
| `account_stage_ids[]` | body | `array<string>` | no | The Apollo IDs for the account stages that you want to include in your search results. If you add multiple account stages, Apollo will include all accounts that match any of the stages, along with the other parameters, in the search results. Call the [List Account Stages endpoint](https://docs.apollo.io/reference/list-account-stages) to retrieve a list of all the account stage IDs available in your Apollo account. Example: `61b8e913e0f4d2012e3af74e` |
| `account_label_ids[]` | body | `array<string>` | no | The Apollo IDs for the labels that you want to include in your search results. If you add multiple labels, Apollo will include all accounts connected to any of the labels, along with the other parameters, in the search results. Example: `['6095a710bd01d100a506d4ae']` |
| `sort_by_field` | body | `string` | no | Sort the matching accounts by 1 of the following options: - `account_last_activity_date`: The most recent activity date recorded first. - `account_created_at`: The most recently created first. - `account_updated_at`: The most recently updated first. |
| `sort_ascending` | body | `boolean` | no | Set to `true` to sort the matching accounts in ascending order. This parameter must be used with `sort_by_field`. Otherwise, the sorting logic is not applied. Example: `true` |
