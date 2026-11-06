# Create Customer Action with Viewpoint Vista

## Endpoint

- **Method:** `POST`
- **Path:** `v1/direct/subscribers/:subscriber_code/vista/:api/2/data/customers/actions/add`
- **Base URL:** `https://api.xchange.trimble.com/connect/`
- **API:** REST
- **Official documentation:** [Create Customer Action](https://direct-api.xchange.trimble.com/reference/post-directsubscriberssubscriber_codevistaar2datacustomersactionsadd)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ARCo` | body | `number` | no | — |
| `BillingAddress.BillAddress` | body | `string` | no | Billing address line 1 (max 60). |
| `BillingAddress.BillAddress2` | body | `string` | no | Billing address line 2 (max 60). |
| `BillingAddress.BillCity` | body | `string` | no | Billing city (max 30). |
| `BillingAddress.BillCountry` | body | `string` | no | Billing country code (2 letters, e.g. US). Defaults to the HQ company default country. |
| `BillingAddress.BillState` | body | `string` | no | Billing state (max 4). Validated by Vista against the states of the BillCountry. |
| `BillingAddress.BillZip` | body | `string` | no | Billing ZIP / postal code (max 12). |
| `CompanyContact.Contact` | body | `string` | no | Contact name (max 30). |
| `CompanyContact.ContactExt` | body | `string` | no | Contact phone extension (max 10). |
| `CompanyContact.EMail` | body | `string` | no | Contact email (max 255). |
| `CompanyContact.Fax` | body | `string` | no | Contact fax (max 20). |
| `CompanyContact.Phone` | body | `string` | no | Contact phone (max 20). |
| `CompanyContact.URL` | body | `string` | no | Contact website URL (max 60). |
| `MailingAddress.Address` | body | `string` | no | Mailing address line 1 (max 60). |
| `MailingAddress.Address2` | body | `string` | no | Mailing address line 2 (max 60). |
| `MailingAddress.City` | body | `string` | no | Mailing city (max 30). |
| `MailingAddress.Country` | body | `string` | no | Mailing country code (2 letters, e.g. US). Defaults to the HQ company default country. |
| `MailingAddress.State` | body | `string` | no | Mailing state (max 4). Validated by Vista against the states of the Country. |
| `MailingAddress.Zip` | body | `string` | no | Mailing ZIP / postal code (max 12). |
| `Customer` | body | `object` | no | — |
| `Name` | body | `string` | no | — |
| `RecType` | body | `number` | no | Receivable Type key for the AR company. Optional; Vista uses the company default when omitted. |
| `MailingAddress` | body | `object` | no | — |
| `BillingAddress` | body | `object` | no | — |
| `PayTerms` | body | `string` | no | — |
| `CompanyContact` | body | `object` | no | — |
| `__custom_fields` | body | `object` | no | — |
| `TaxCode` | body | `string` | no | — |
| `SortName` | body | `string` | no | Customer sort name (max 15 characters). If omitted, Vista calculates it from the name and appends trailing digits when the result is not unique. Maximum length: 15. |
| `Status` | body | `string` | no | Customer status: A = Active, I = Inactive, H = On Hold. Defaults to A when omitted. Maximum length: 1. |
| `DateOpened` | body | `string` | no | Date the customer was opened, in YYYY-MM-DD format (date only, no time). Defaults to today's date when omitted. Maximum length: 10. |
