# Get Account with Dropbox

Retrieves an account's details from Dropbox.

## Endpoint

- **Method:** `POST`
- **Path:** `/users/get_account`
- **Base URL:** `https://api.dropboxapi.com/2`
- **Official documentation:** [Get Account](https://www.dropbox.com/developers/documentation/http/documentation#users-get_account)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_id` | body | `string` | yes | The account ID to look up. |
