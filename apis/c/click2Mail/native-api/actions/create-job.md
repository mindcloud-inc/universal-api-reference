# Create Job with Click2Mail

Creates a new job in Click2Mail.

## Endpoint

- **Method:** `POST`
- **Path:** `/molpro/jobs`
- **Base URL:** `https://stage-rest.click2mail.com`
- **Official documentation:** [Create Job](https://developers.click2mail.com/reference/post_2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentClass` | query | `string` | yes | The general type of the product |
| `layout` | query | `string` | yes | The specific type of the product |
| `productionTime` | query | `string` | yes | The desired production time |
| `envelope` | query | `string` | yes | If this is an enveloped product this determines the envelope in which the product is to be mailed; otherwise provide no value |
| `color` | query | `string` | yes | Print in color or black and white |
| `paperType` | query | `string` | yes | Sets the paper the mailing is to be printed on |
| `printOption` | query | `string` | yes | Sets simplex or duplex printing |
| `documentId` | query | `string` | no | ID of the document to print |
| `addressId` | query | `string` | no | This required if the product required a recipient address list |
| `rtnName` | query | `string` | no | Return address Name |
| `rtnOrganization` | query | `string` | no | Return address Organization |
| `rtnaddress1` | query | `string` | no | Return address line 1 |
| `rtnaddress2` | query | `string` | no | Return address line 2 |
| `rtnCity` | query | `string` | no | Return address City |
| `rtnState` | query | `string` | no | Return address state |
| `rtnZip` | query | `string` | no | Return address zip code |
| `endorsement` | query | `string` | no | Ancillary endorsement service, the default is none |
| `mailClass` | query | `string` | no | Overrides the default of First Class for mailed products |
| `appSignature` | query | `string` | no | This is a short signature to identify orders that come from your app |
| `projectId` | query | `number` | no | use to place this job in a pre-existing project in your account |
| `mailingDate` | query | `string` | no | Used to schedule the mailing date in the future. Format YYYYMMDD. If not provided the order will be mailed on the next available on the next business day. The business day cut off is 8PM EST. |
| `quantity` | query | `string` | no | For products that do not use mailing lists. Quantity to print |
| `jobDocumentId` | query | `string` | no | document ID of the job version of the document |
| `jobAddressId` | query | `string` | no | Address List Id of the job version |
| `businessReplyAddressId` | query | `number` | no | If you are mailing a business reply mail product use this to specify the busines reply address and permit information already in your account |
| `courtesyReplyAddressId` | query | `number` | no | If you are mailing a courtesy reply mail product use this to specify a courtesy reply address already in your account |
| `returnAddressId` | query | `number` | no | You may use the return address id to specify a return address already in your account |
| `enclosure` | query | `string` | no | Identifies the special encloure to use with this order. Special enclosures must be pre-arranged with Click2Mail |
