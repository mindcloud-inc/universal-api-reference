# Create Account Address with Click2Mail

Creates a new account address in Click2Mail.

## Endpoint

- **Method:** `POST`
- **Path:** `/molpro/account/addresses`
- **Base URL:** `https://stage-rest.click2mail.com`
- **Official documentation:** [Create Account Address](https://developers.click2mail.com/reference/createaccountaddresses)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `type` | query | `string` | yes |
| `prefix` | query | `string` | no |
| `suffix` | query | `string` | no |
| `description` | query | `string` | yes |
| `makeDefault` | query | `string` | no |
| `firstName` | query | `string` | no |
| `middleName` | query | `string` | no |
| `lastName` | query | `string` | no |
| `address1` | query | `string` | yes |
| `address2` | query | `string` | no |
| `address3` | query | `string` | no |
| `city` | query | `string` | yes |
| `state` | query | `string` | no |
| `zip` | query | `string` | no |
| `phone` | query | `string` | no |
| `permitNumber` | query | `string` | no |
| `replyCity` | query | `string` | no |
| `replyRegionId` | query | `string` | no |
| `organization` | query | `string` | no |
| `country` | query | `string` | no |
