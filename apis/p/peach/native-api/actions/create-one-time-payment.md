# Create One-Time Payment with Peach

Creates a one-time payment in Peach.

## Endpoint

- **Method:** `POST`
- **Path:** `/payments`
- **Base URL:** `https://api.peach-in.com/v4`
- **Official documentation:** [Create One-Time Payment](https://peach-organization.gitbook.io/peach/api-reference/payments/create-payment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sum` | body | `number` | yes | Payment sum. |
| `firstName` | body | `string` | no | Donor first name. |
| `lastName` | body | `string` | no | Donor last name. |
| `email` | body | `string` | no | Donor email address. |
| `phone` | body | `string` | no | Donor phone number. |
| `displayName` | body | `string` | no | Display name for the donor. |
| `currency` | body | `string` | no | Donation currency. Peach defaults to ILS. |
| `campaignId` | body | `string` | no | Campaign ID for the payment. |
| `groupId` | body | `string` | no | Group ID for the payment. |
| `contactId` | body | `string` | no | Existing Peach contact ID for the donor. |
| `customProperties` | body | `object` | no | Custom properties for the payment. |
| `triggerAutomations` | body | `boolean` | no | Set to true only if the payment should trigger automations in Peach. |
