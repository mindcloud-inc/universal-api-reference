# Update Account Address with Click2Mail

Updates an existing account address in Click2Mail.

## Endpoint

- **Method:** `POST`
- **Path:** `/molpro/account/addresses/{addressId}`
- **Base URL:** `https://stage-rest.click2mail.com`
- **Official documentation:** [Update Account Address](https://developers.click2mail.com/reference/updateaccountaddresses)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `addressId` | path | `string` | yes | — |
| `description` | query | `string` | yes | The name to identify this address |
| `makeDefault` | query | `string` | no | A Yes indicates that this address is to be made the default address in this type |
| `type` | query | `string` | yes | — |
| `prefix` | query | `string` | no | — |
| `firstName` | query | `string` | no | First Name |
| `middleName` | query | `string` | no | Middle Initial |
| `lastName` | query | `string` | no | Last Name |
| `suffix` | query | `string` | no | — |
| `address1` | query | `string` | yes | Address line 1 |
| `address2` | query | `string` | no | Address line 2 |
| `address3` | query | `string` | no | Address line 3 |
| `city` | query | `string` | yes | City |
| `state` | query | `string` | no | State |
| `zip` | query | `string` | no | Postal Code |
| `phone` | query | `string` | no | Contract phone number for this address. Required for EDDM mailer address, Must be properly formatted. For example XXX-XXX-XXXX or XXX-XXX-XXXX ext XXXX format. |
| `permitNumber` | query | `string` | no | Required for Business Reply address |
| `replyCity` | query | `string` | no | Required for Business Reply addresses |
| `replyRegionId` | query | `string` | no | Required for Business Reply address |
| `organization` | query | `string` | no | Company Name |
| `country` | query | `string` | no | country |
