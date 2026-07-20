# Retrieve a Contact by an Identifier with Dotdigital

Retrieves a contact from Dotdigital by a specified identifier.

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts/v3/:identifier/:value`
- **Base URL:** `https://r2-api.dotmailer.com`
- **Official documentation:** [Retrieve a Contact by an Identifier](https://developer.dotdigital.com/reference/getcontact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifier` | path | `string` | yes | Use contactId, email, mobileNumber, or a custom identifier. |
| `value` | path | `string` | yes | The value for the selected identifier. |
