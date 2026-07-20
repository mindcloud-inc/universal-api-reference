# Get Cost Estimate with Click2Mail

Retrieves a mailing cost estimate from Click2Mail.

## Endpoint

- **Method:** `GET`
- **Path:** `/molpro/costEstimate`
- **Base URL:** `https://stage-rest.click2mail.com`
- **Official documentation:** [Get Cost Estimate](https://developers.click2mail.com/reference/getcostestimate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentClass` | query | `string` | yes | The general type of the product |
| `layout` | query | `string` | yes | The specific type of the product |
| `productionTime` | query | `string` | yes | The desired production time |
| `envelope` | query | `string` | yes | If this is an enveloped product this determines the envelope in which the product is to be mailed; otherwise provide no description |
| `color` | query | `string` | yes | Print in color or black and white |
| `paperType` | query | `string` | yes | Sets the paper the mailing is to be printed on |
| `printOption` | query | `string` | yes | Sets simplex or duplex printing |
| `mailClass` | query | `string` | no | If the product is mailed how do you want it mailed |
| `quantity` | query | `number` | no | How many do you want printed |
| `nonStandardQuantity` | query | `number` | no | How may non-standard addresses |
| `internationalQuantity` | query | `number` | no | How many international addresses |
| `numberOfPages` | query | `number` | no | How many pages in your document |
| `paymentType` | query | `string` | no | Default is Credit Card |
| `couponCode` | query | `string` | no | Coupon Code |
