# Find Recipient with Onfleet

Finds a recipient in Onfleet by name or phone.

## Endpoint

- **Method:** `GET`
- **Path:** `/recipients/:lookupType/:lookupValue`
- **Base URL:** `https://onfleet.com/api/v2`
- **Official documentation:** [Find Recipient](https://docs.onfleet.com/reference/find-recipient)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lookupType` | path | `string` | yes | Which recipient property to search by. Use name or phone. |
| `lookupValue` | path | `string` | yes | The exact recipient name or phone number to look up. |
| `skipPhoneNumberValidation` | query | `boolean` | no | When true, bypasses phone validation for recipients created without validation. |
