# Find Account By Email with Billforward

Finds an account in Billforward by email address.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/email/:email`
- **Base URL:** `https://app-sandbox.billforward.net/v1`
- **Official documentation:** [Find Account By Email](https://app.billforward.net/#/api/method/accounts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | path | `string` | yes | The Billforward account email to search for. |
