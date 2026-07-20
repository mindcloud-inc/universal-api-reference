# List Contacts with Billage

Retrieves contact records from Billage by criteria.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/contacts`
- **Base URL:** `https://app.getbillage.com/api`
- **Official documentation:** [List Contacts](https://app.getbillage.com/api/documentation.html#/Contacts/contactsByParameters)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | no | Search contacts |
| `name` | query | `string` | no | Contact name |
| `surname` | query | `string` | no | Contact surname |
| `email` | query | `string` | no | Contact email |
| `phone` | query | `string` | no | Contact phone 1 |
| `account` | query | `string` | no | Contact account |
| `account-id` | query | `number` | no | Contact account ID |
| `account-type` | query | `string` | no | Contact account type |
| `colour` | query | `string` | no | Colour name |
| `owner` | query | `string` | no | Contact owner |
| `tags[]` | query | `array<string>` | no | Contact tags |
