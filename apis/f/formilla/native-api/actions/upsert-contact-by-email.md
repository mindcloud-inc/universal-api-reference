# Create or Update Contact (Email Required) with Formilla

Creates or updates a contact in Formilla by email address.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts`
- **Base URL:** `https://api.formilla.com/api`
- **Official documentation:** [Create or Update Contact (Email Required)](https://blog.formilla.com/integrate-customer-data-with-the-formilla-rest-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Email` | body | `string` | yes | — |
| `FirstName` | body | `string` | no | — |
| `LastName` | body | `string` | no | — |
| `Phone` | body | `string` | no | — |
| `SignedUp_date` | body | `number` | no | Unix timestamp for when the contact signed up. |
| `IsUnsubscribed` | body | `boolean` | no | — |
| `CustomAttributes` | body | `object` | no | JSON object with custom contact key/value pairs. |
