# Create Client with InventoryBase

Creates a new client in InventoryBase.

## Endpoint

- **Method:** `POST`
- **Path:** `/clients`
- **Base URL:** `https://api.inventorybase.com`
- **Official documentation:** [Create Client](https://developer.inventorybase.com/#create-a-client)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The client's full name. |
| `email` | body | `string` | yes | The client's email address. |
| `address` | body | `object` | yes | The client's primary address object. |
| `telephone` | body | `string` | no | The client's telephone number. |
| `company` | body | `string` | no | The client's company name. |
| `website` | body | `string` | no | The client's website. |
| `notes` | body | `string` | no | Notes about the client. |
| `send_login_details` | body | `boolean` | no | Whether to send login details to the new client. |
| `email_notifications` | body | `boolean` | no | Whether the client should receive email notifications. |
| `ignore_welcome_mailer` | body | `boolean` | no | Whether to suppress the initial welcome email. |
