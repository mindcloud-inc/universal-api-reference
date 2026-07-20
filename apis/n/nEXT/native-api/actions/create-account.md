# Create Account with NEXT

Creates a new account in NEXT.

## Endpoint

- **Method:** `POST`
- **Path:** `/accounts`
- **Base URL:** `https://rest.eu-west-1.nextapp.co/v1`
- **Official documentation:** [Create Account](https://developer.nextapp.co/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The account name. |
| `account_type` | body | `string` | no | The account type label. |
| `status` | body | `string` | no | The account status. |
