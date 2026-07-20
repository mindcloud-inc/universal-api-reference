# Opt-In SMS Contact with Customers.ai

Opts a new SMS contact into a promoter in Customers.ai.

## Endpoint

- **Method:** `PUT`
- **Path:** `/promoters/:id/optin_sms_contact`
- **Base URL:** `https://api.mobilemonkey.com/public`
- **Official documentation:** [Opt-In SMS Contact](https://customers.ai/help/l/en/category/doq3ewxla3-public-api)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Promoter ID to use for the SMS opt-in flow. |
| `sms_number` | body | `string` | yes | Phone number to opt in. |
| `first_name` | body | `string` | no | First name of the SMS contact. |
| `last_name` | body | `string` | no | Last name of the SMS contact. |
