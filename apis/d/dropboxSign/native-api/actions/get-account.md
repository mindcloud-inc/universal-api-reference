# Get Account with Dropbox Sign

Retrieves your Dropbox Sign account settings.

## Endpoint

- **Method:** `GET`
- **Path:** `/account`
- **Base URL:** `https://api.hellosign.com/v3`
- **Official documentation:** [Get Account](https://developers.hellosign.com/api/reference/operation/accountGet/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_id` | query | `string` | no | The ID of the account to retrieve. If both Account ID and Email Address are provided, Account ID wins. |
| `email_address` | query | `string` | no | The email address of the account to retrieve when Account ID is not provided. |
