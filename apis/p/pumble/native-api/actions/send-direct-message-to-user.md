# Send Direct Message to User with Pumble

Creates a direct message to a Pumble user.

## Endpoint

- **Method:** `POST`
- **Path:** `/dmUser`
- **Base URL:** `https://pumble-api-keys.addons.marketplace.cake.com`
- **Official documentation:** [Send Direct Message to User](https://pumble-api-keys.addons.marketplace.cake.com/api-docs/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `email` | body | `string` | no |
| `text` | body | `string` | yes |
| `userId` | body | `string` | no |
