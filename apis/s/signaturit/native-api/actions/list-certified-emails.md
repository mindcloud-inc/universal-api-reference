# List Certified Emails with Signaturit

Retrieves certified emails from Signaturit.

## Endpoint

- **Method:** `GET`
- **Path:** `/emails.json`
- **Base URL:** `https://api.sandbox.signaturit.com/v3`
- **API:** rest
- **Official documentation:** [List Certified Emails](https://docs.signaturit.com/api/latest#emails_get_emails)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Max number of emails to retrieve. |
| `offset` | query | `number` | no | Results offset. |
| `status` | query | `string` | no | Filter emails by status. |
| `since` | query | `string` | no | Return emails sent on or after this date. |
