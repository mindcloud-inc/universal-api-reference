# Click2Mail: Native API Reference

A consolidated summary of Click2Mail's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://developers.click2mail.com/reference
- **API base URL:** `https://stage-rest.click2mail.com`

## Authentication

### Basic Auth

Use your Click2Mail API username and password.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://developers.click2mail.com/docs/building-your-first-api-call)

## API conventions

Request bodies use XML.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/xml` |
| `Content-Type` | `application/xml` |

Responses from this API use XML.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Accept Proof](actions/accept-proof.md) | `POST /molpro/jobs/{id}/proof/accept` | [docs](https://developers.click2mail.com/reference/acceptproof) |
| [Add Address Book Addresses](actions/add-address-book-addresses.md) | `POST /molpro/addressBook/{id}/address` | [docs](https://developers.click2mail.com/reference/addaddresses_1) |
| [Add Address List Addresses](actions/add-address-list-addresses.md) | `POST /molpro/addressLists/address2` | [docs](https://developers.click2mail.com/reference/addaddresses) |
| [Add Addresses From Address Book](actions/add-addresses-from-address-book.md) | `POST /molpro/addressLists/address/addressBook` | [docs](https://developers.click2mail.com/reference/addaddressesfromaddressbook) |
| [Add Addresses To Mailing List](actions/add-addresses-to-mailing-list.md) | `POST /molpro/addressLists/address` | [docs](https://developers.click2mail.com/reference/addaddressestomaillist) |
| [Check Address List Name](actions/check-address-list-name.md) | `POST /molpro/addressLists/checkName` | [docs](https://developers.click2mail.com/reference/validateaddresslistname) |
| [Check Credit Balance](actions/check-credit-balance.md) | `GET /molpro/credit` | [docs](https://developers.click2mail.com/reference/getuser) |
| [Check Document Name](actions/check-document-name.md) | `POST /molpro/documents/checkName` | [docs](https://developers.click2mail.com/reference/checkdocumentname) |
| [Convert Document To PDF](actions/convert-document-to-pdf.md) | `POST /molpro/documents/convertToPdf` | [docs](https://developers.click2mail.com/reference/wordtopdf) |
| [Create Account Address](actions/create-account-address.md) | `POST /molpro/account/addresses` | [docs](https://developers.click2mail.com/reference/createaccountaddresses) |
| [Create Address Book](actions/create-address-book.md) | `POST /molpro/addressBook` | [docs](https://developers.click2mail.com/reference/createaddressbook) |
| [Create Address List](actions/create-address-list.md) | `POST /molpro/addressLists` | [docs](https://developers.click2mail.com/reference/createaddresslist) |
| [Create Document](actions/create-document.md) | `POST /molpro/documents` | [docs](https://developers.click2mail.com/reference/createdocument_1) |
| [Create Document From URL](actions/create-document-from-url.md) | `POST /molpro/documents/url` | [docs](https://developers.click2mail.com/reference/createdocumentfromurl) |
| [Create Job](actions/create-job.md) | `POST /molpro/jobs` | [docs](https://developers.click2mail.com/reference/post_2) |
| [Create Proof](actions/create-proof.md) | `POST /molpro/jobs/{id}/proof` | [docs](https://developers.click2mail.com/reference/createproof) |
| [Delete Address Book](actions/delete-address-book.md) | `DELETE /molpro/addressBook/{id}` | [docs](https://developers.click2mail.com/reference/deleteaddressbook) |
| [Delete Address List](actions/delete-address-list.md) | `DELETE /molpro/addressLists/{id}` | [docs](https://developers.click2mail.com/reference/deleteaddresslist) |
| [Delete Addresses From List](actions/delete-addresses-from-list.md) | `DELETE /molpro/addressLists` | [docs](https://developers.click2mail.com/reference/deleteaddresses) |
| [Get Address Book](actions/get-address-book.md) | `GET /molpro/addressBook/{id}` | [docs](https://developers.click2mail.com/reference/getaddressdetails) |
| [Get Address List](actions/get-address-list.md) | `GET /molpro/addressLists/{id}` | [docs](https://developers.click2mail.com/reference/getaddressliststatus) |
| [Get Address List Info](actions/get-address-list-info.md) | `GET /molpro/addressLists/info` | [docs](https://developers.click2mail.com/reference/getaddresslistinfo) |
| [Get Cost Estimate](actions/get-cost-estimate.md) | `GET /molpro/costEstimate` | [docs](https://developers.click2mail.com/reference/getcostestimate) |
| [Get Document Variable Data](actions/get-document-variable-data.md) | `GET /molpro/documents/variableData/{id}` | [docs](https://developers.click2mail.com/reference/getvariabledatabydocumentid) |
| [Get Job](actions/get-job.md) | `GET /molpro/jobs/{id}` | [docs](https://developers.click2mail.com/reference/getjob) |
| [Get Job Cost](actions/get-job-cost.md) | `GET /molpro/jobs/{id}/cost` | [docs](https://developers.click2mail.com/reference/getjobcost) |
| [Get Job Info](actions/get-job-info.md) | `GET /molpro/jobs/info/{id}` | [docs](https://developers.click2mail.com/reference/getjobinfo) |
| [Get Proof](actions/get-proof.md) | `GET /molpro/jobs/{id}/proof/{proofId}/{sessionId}` | [docs](https://developers.click2mail.com/reference/getproof) |
| [List Account Addresses](actions/list-account-addresses.md) | `GET /molpro/account/addresses` | [docs](https://developers.click2mail.com/reference/getaccountaddresses) |
| [List Address Books](actions/list-address-books.md) | `GET /molpro/addressBook` | [docs](https://developers.click2mail.com/reference/getaddressbooks) |
| [List Address Lists](actions/list-address-lists.md) | `GET /molpro/addressLists` | [docs](https://developers.click2mail.com/reference/getaddresslist) |
| [List Documents](actions/list-documents.md) | `GET /molpro/documents` | [docs](https://developers.click2mail.com/reference/getdocuments) |
| [List Job Documents](actions/list-job-documents.md) | `GET /molpro/documents/jobDocuments` | [docs](https://developers.click2mail.com/reference/getjobdocuments) |
| [List Jobs](actions/list-jobs.md) | `GET /molpro/jobs` | [docs](https://developers.click2mail.com/reference/getjobs_1) |
| [Merge Document](actions/merge-document.md) | `POST /molpro/documents/merge` | [docs](https://developers.click2mail.com/reference/mergedocument) |
| [Submit Job](actions/submit-job.md) | `POST /molpro/jobs/{id}/submit` | [docs](https://developers.click2mail.com/reference/submitjob) |
| [Update Account Address](actions/update-account-address.md) | `POST /molpro/account/addresses/{addressId}` | [docs](https://developers.click2mail.com/reference/updateaccountaddresses) |
| [Update Address Book Addresses](actions/update-address-book-addresses.md) | `PUT /molpro/addressBook/{id}/address` | [docs](https://developers.click2mail.com/reference/updateaddresses_1) |
| [Update Address List Addresses](actions/update-address-list-addresses.md) | `PUT /molpro/addressLists/address2` | [docs](https://developers.click2mail.com/reference/updateaddresses) |
| [Update Job](actions/update-job.md) | `POST /molpro/jobs/{id}/update` | [docs](https://developers.click2mail.com/reference/updatejob) |
