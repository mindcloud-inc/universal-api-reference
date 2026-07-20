# Create Donation with Pledge

Creates a donation in Pledge.

## Endpoint

- **Method:** `POST`
- **Path:** `/donations`
- **Base URL:** `https://api.pledge.to/v1`
- **Official documentation:** [Create Donation](https://developer.pledge.to/api/#tag/Donations/operation/createDonation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Donor email address. |
| `first_name` | body | `string` | yes | Donor first name. |
| `last_name` | body | `string` | yes | Donor last name. |
| `amount` | body | `string` | yes | Donation amount. |
| `organization_id` | body | `string` | yes | Beneficiary organization ID. |
| `phone_number` | body | `string` | no | Donor phone number. |
| `metadata` | body | `string` | no | Arbitrary provider metadata string. |
| `send_tax_receipt` | body | `boolean` | no | Whether to email a tax receipt to the donor. |
