# Submit Job with Click2Mail

Submits an existing job in Click2Mail.

## Endpoint

- **Method:** `POST`
- **Path:** `/molpro/jobs/{id}/submit`
- **Base URL:** `https://stage-rest.click2mail.com`
- **Official documentation:** [Submit Job](https://developers.click2mail.com/reference/submitjob)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | job id |
| `billingType` | query | `string` | yes | Payment Method |
| `billingName` | query | `string` | no | Name as on the card, Required (Credit Card only) |
| `billingCompany` | query | `string` | no | Company |
| `billingAddress1` | query | `string` | no | Street address line 1, Required (Credit Card only) |
| `billingAddress2` | query | `string` | no | Street address line 2 |
| `billingAddress3` | query | `string` | no | Street address line 3 |
| `billingCity` | query | `string` | no | City, Required (Credit Card only) |
| `billingState` | query | `string` | no | State, Required (Credit Card only) |
| `billingCountry` | query | `string` | no | Requires for non USA addresses |
| `billingZip` | query | `string` | no | Zip code, Required (Credit Card only) |
| `billingNumber` | query | `string` | no | Credit card number, Required (Credit Card only) |
| `billingMonth` | query | `string` | no | Expiration month, 2 digits, Required (Credit Card only) |
| `billingYear` | query | `string` | no | Expiration year, 2 digits, Required (Credit Card only) |
| `billingCvv` | query | `string` | no | Credit card verification code, 3 digits, Required (Credit Card only) |
| `billingCcType` | query | `string` | no | Credit card type, Required (Credit Card only) |
| `shipName` | query | `string` | no | Shipping address Name |
| `shipOrganization` | query | `string` | no | Shipping address Organization |
| `shipAddress1` | query | `string` | no | Shipping address line 1 |
| `shipaddress2` | query | `string` | no | Shipping address line 2 |
| `shipCity` | query | `string` | no | Ship address City |
| `shipState` | query | `string` | no | Ship address State |
| `shipZip` | query | `string` | no | Ship address Zip code |
| `shipCountry` | query | `string` | no | Leave blank for USA |
| `shipperName` | query | `string` | no | Shipper |
| `shipMethod` | query | `string` | no | Shipping Method |
| `couponCode` | query | `string` | no | Coupon Code for order |
| `opaqueDataValue` | query | `string` | no | Apple Pay/Google Pay opaque Data Value |
