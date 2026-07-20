# List Site Contacts with Fingertip

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/site-contacts`
- **Base URL:** `https://api.fingertip.com`
- **Official documentation:** [List Site Contacts](https://docs.fingertip.com/openapi-specs/list-site-contacts.md)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `siteId` | query | `string` | yes | Site ID. |
| `search` | query | `string` | no | Search query. |
| `marketingStatuses[]` | query | `array<string>` | no | Marketing status filters. |
| `hasSegmentation` | query | `boolean` | no | Whether the contact has segmentation. |
| `hasRatings` | query | `boolean` | no | Whether the contact has ratings. |
| `hasFormResponses` | query | `boolean` | no | Whether the contact has form responses. |
| `hasAppointments` | query | `boolean` | no | Whether the contact has appointments. |
| `hasOrders` | query | `boolean` | no | Whether the contact has orders. |
| `hasInvoices` | query | `boolean` | no | Whether the contact has invoices. |
| `hasQuotes` | query | `boolean` | no | Whether the contact has quotes. |
| `hasPayments` | query | `boolean` | no | Whether the contact has payments. |
| `createdAfter` | query | `string` | no | Only contacts created after this timestamp. |
