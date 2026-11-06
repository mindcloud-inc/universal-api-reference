# Update Customer Action with Viewpoint Vista

## Endpoint

- **Method:** `POST`
- **Path:** `v1/direct/subscribers/:subscriber_code/vista/:api/2/data/customers/actions/change`
- **Base URL:** `https://api.xchange.trimble.com/connect/`
- **API:** REST
- **Official documentation:** [Update Customer Action](https://direct-api.xchange.trimble.com/reference/post-directsubscriberssubscriber_codevistaar2datacustomersactionschange)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ARCo` | body | `number` | no | — |
| `BillingAddress.BillAddress` | body | `string` | no | Billing address line 1 (max 60). |
| `BillingAddress.BillAddress2` | body | `string` | no | Billing address line 2 (max 60). |
| `BillingAddress.BillCity` | body | `string` | no | Billing city (max 30). |
| `BillingAddress.BillCountry` | body | `string` | no | Billing country code (2 letters, e.g. US). |
| `BillingAddress.BillState` | body | `string` | no | Billing state (max 4). Validated by Vista against the states of the BillCountry. |
| `BillingAddress.BillZip` | body | `string` | no | Billing ZIP / postal code (max 12). |
| `CompanyContact.Phone` | body | `string` | no | — |
| `MailingAddress.Address` | body | `string` | no | Mailing address line 1 (max 60). |
| `MailingAddress.Address2` | body | `string` | no | Mailing address line 2 (max 60). |
| `MailingAddress.City` | body | `string` | no | Mailing city (max 30). |
| `MailingAddress.Country` | body | `string` | no | Mailing country code (2 letters, e.g. US). |
| `MailingAddress.State` | body | `string` | no | Mailing state (max 4). Validated by Vista against the states of the Country. |
| `MailingAddress.Zip` | body | `string` | no | Mailing ZIP / postal code (max 12). |
| `CompanyContact.Fax` | body | `string` | no | — |
| `Name` | body | `string` | no | — |
| `CompanyContact.Contact` | body | `string` | no | — |
| `RecType` | body | `number` | no | Receivable Type key for the AR company. Optional; Vista uses the company default when omitted. |
| `CompanyContact.ContactExt` | body | `string` | no | — |
| `MailingAddress` | body | `object` | no | — |
| `BillingAddress` | body | `object` | no | — |
| `CompanyContact.EMail` | body | `string` | no | — |
| `CompanyContact.URL` | body | `string` | no | — |
| `PayTerms` | body | `string` | no | — |
| `TaxCode` | body | `string` | no | — |
| `CompanyContact` | body | `object` | no | — |
| `__key` | body | `object` | no | Identifies the customer to change. Required. Use exactly one of two forms: { "KeyID": 12345 } (surrogate key) or { "CustGroup": 1, "Customer": 1001 } (natural key; CustGroup must match the one of the ARCo in HQ company parameters). Each form accepts only its own properties. |
| `__custom_fields` | body | `object` | no | — |
| `SortName` | body | `string` | no | New customer sort name (max 15 characters). Only sent properties are changed. Maximum length: 15. |
| `Status` | body | `string` | no | New customer status: A = Active, I = Inactive, H = On Hold. Only sent properties are changed. Maximum length: 1. |
| `DateOpened` | body | `string` | no | New date opened, in YYYY-MM-DD format (date only, no time). Only sent properties are changed. Maximum length: 10. |
