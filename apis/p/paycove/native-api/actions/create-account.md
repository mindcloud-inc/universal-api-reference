# Create Account with Paycove

Creates an account in Paycove.

## Endpoint

- **Method:** `POST`
- **Path:** `accounts`
- **Base URL:** `https://paycove.io/api/v1`
- **Official documentation:** [Create Account](https://docs.paycove.io/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `country_code` | body | `string` | yes | Two-letter country code for the account. |
| `currency` | body | `string` | yes | The account currency. |
| `legal_acceptance_token` | body | `string` | yes | The legal acceptance token returned by the legal-accept flow. |
| `name` | body | `string` | yes | The account name. |
| `phone` | body | `string` | no | The account phone number. |
| `platform_fee` | body | `number` | no | Platform fee percentage. |
| `template` | body | `object` | no | Template settings for the account. |
| `timezone` | body | `string` | yes | The account timezone. |
| `user` | body | `object` | no | The initial account user to create. |
