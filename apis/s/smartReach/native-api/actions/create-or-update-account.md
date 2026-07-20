# Create or Update Account with SmartReach

Finds an account in SmartReach, or creates one if needed.

## Endpoint

- **Method:** `POST`
- **Path:** `/accounts`
- **Base URL:** `https://api.smartreach.io/api/v3`
- **Official documentation:** [Create or Update Account](https://help.smartreach.io/reference/post_accounts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Name of the account |
| `custom_id` | body | `string` | no | custom_id of the account |
| `description` | body | `string` | no | description of the account |
| `website` | body | `string` | no | website of the account |
| `industry` | body | `string` | no | industry of the account |
| `linkedin_url` | body | `string` | no | linkedin_url of the account |
| `custom_fields` | body | `object` | no | custom_fields of the account |
| `update_account` | body | `string` | no | option for update account |
