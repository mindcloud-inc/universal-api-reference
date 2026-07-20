# Create or Update Contact (User ID Required) with Formilla

Creates or updates a contact in Formilla by user ID.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts`
- **Base URL:** `https://api.formilla.com/api`
- **Official documentation:** [Create or Update Contact (User ID Required)](https://blog.formilla.com/integrate-customer-data-with-the-formilla-rest-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `UserId` | body | `string` | yes | A unique identifier for the contact. |
| `Email` | body | `string` | no | The contact's email address. |
| `FirstName` | body | `string` | no | — |
| `LastName` | body | `string` | no | — |
| `Phone` | body | `string` | no | — |
| `SignedUp_date` | body | `number` | no | Unix timestamp for when the contact signed up. |
| `IsUnsubscribed` | body | `boolean` | no | — |
| `CustomAttributes` | body | `object` | no | JSON object with custom contact key/value pairs. |
