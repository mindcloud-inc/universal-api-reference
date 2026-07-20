# SAP ERP (S/4HANA): Native API Reference

A consolidated summary of SAP ERP (S/4HANA)'s API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://api.sap.com/api/API_BUSINESS_PARTNER/overview
- **OpenAPI specification:** https://api.sap.com/odata/1.0/catalog.svc/APIContent.APIs('API_BUSINESS_PARTNER')/$value?type=json
- **API base URL:** `https://sandbox.api.sap.com/s4hanacloud/sap/opu/odata/sap/API_BUSINESS_PARTNER`

## Authentication

### SAP Business Accelerator Hub API Key

SAP Business Accelerator Hub sandbox API key sent in the APIKey request header.

### Credentials

- **API Key:** `apiKey` · required · SAP Business Accelerator Hub sandbox API key used for the APIKey request header.

[Official authentication documentation](https://help.sap.com/docs/business-accelerator-hub/sap-business-accelerator-hub/trying-out-apis-in-sandbox-environment)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The next-page cursor is read from `d.__next`.

## Pagination

Use `$top` in the query string to set the page size (default 10; accepted range 1–100). Use `$skip` in the query string as the record offset; numbering starts at 0.

## Filtering

Send filters in the query string. Supported operators: `eq`.

## Sorting

Set the sort field with `$orderby` in the query string. Multiple sort fields can be combined.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Business Partner](actions/get-business-partner.md) | `GET /A_BusinessPartner('{{businessPartner}}')` | [docs](https://api.sap.com/api/API_BUSINESS_PARTNER) |
| [Get Business Partner Bank Profile](actions/get-business-partner-bank-profile.md) | `GET /A_BusinessPartner('{{businessPartner}}')/to_BusinessPartnerIsBank` | [docs](https://api.sap.com/api/API_BUSINESS_PARTNER) |
| [Get Business Partner Credit Worthiness](actions/get-business-partner-credit-worthiness.md) | `GET /A_BusinessPartner('{{businessPartner}}')/to_BPCreditWorthiness` | [docs](https://api.sap.com/api/API_BUSINESS_PARTNER) |
| [Get Customer for Business Partner](actions/get-customer-for-business-partner.md) | `GET /A_BusinessPartner('{{businessPartner}}')/to_Customer` | [docs](https://api.sap.com/api/API_BUSINESS_PARTNER) |
| [Get Related Business Partner](actions/get-related-business-partner.md) | `GET /A_BusinessPartner('{{businessPartner}}')/to_BusinessPartner` | [docs](https://api.sap.com/api/API_BUSINESS_PARTNER) |
| [Get Supplier for Business Partner](actions/get-supplier-for-business-partner.md) | `GET /A_BusinessPartner('{{businessPartner}}')/to_Supplier` | [docs](https://api.sap.com/api/API_BUSINESS_PARTNER) |
| [List Address-Dependent Tax Numbers](actions/list-address-dependent-tax-numbers.md) | `GET /A_BusinessPartner('{{businessPartner}}')/to_BusPartAddrDepdntTaxNmbr` | [docs](https://api.sap.com/api/API_BUSINESS_PARTNER) |
| [List Address Independent Emails](actions/list-address-independent-emails.md) | `GET /A_BusinessPartner('{{businessPartner}}')/to_AddressIndependentEmail` | [docs](https://api.sap.com/api/API_BUSINESS_PARTNER) |
| [List Address Independent Faxes](actions/list-address-independent-faxes.md) | `GET /A_BusinessPartner('{{businessPartner}}')/to_AddressIndependentFax` | [docs](https://api.sap.com/api/API_BUSINESS_PARTNER) |
| [List Address Independent Mobiles](actions/list-address-independent-mobiles.md) | `GET /A_BusinessPartner('{{businessPartner}}')/to_AddressIndependentMobile` | [docs](https://api.sap.com/api/API_BUSINESS_PARTNER) |
| [List Address Independent Phones](actions/list-address-independent-phones.md) | `GET /A_BusinessPartner('{{businessPartner}}')/to_AddressIndependentPhone` | [docs](https://api.sap.com/api/API_BUSINESS_PARTNER) |
| [List Address Independent Websites](actions/list-address-independent-websites.md) | `GET /A_BusinessPartner('{{businessPartner}}')/to_AddressIndependentWebsite` | [docs](https://api.sap.com/api/API_BUSINESS_PARTNER) |
| [List Business Partner Address Emails](actions/list-business-partner-address-emails.md) | `GET /A_BusinessPartnerAddress(BusinessPartner='{{businessPartner}}',AddressID='{{addressId}}')/to_EmailAddress` | [docs](https://api.sap.com/api/API_BUSINESS_PARTNER) |
| [List Business Partner Address Phones](actions/list-business-partner-address-phones.md) | `GET /A_BusinessPartnerAddress(BusinessPartner='{{businessPartner}}',AddressID='{{addressId}}')/to_PhoneNumber` | [docs](https://api.sap.com/api/API_BUSINESS_PARTNER) |
| [List Business Partner Addresses](actions/list-business-partner-addresses.md) | `GET /A_BusinessPartner('{{businessPartner}}')/to_BusinessPartnerAddress` | [docs](https://api.sap.com/api/API_BUSINESS_PARTNER) |
| [List Business Partner Aliases](actions/list-business-partner-aliases.md) | `GET /A_BusinessPartner('{{businessPartner}}')/to_BusinessPartnerAlias` | [docs](https://api.sap.com/api/API_BUSINESS_PARTNER) |
| [List Business Partner Banks](actions/list-business-partner-banks.md) | `GET /A_BusinessPartner('{{businessPartner}}')/to_BusinessPartnerBank` | [docs](https://api.sap.com/api/API_BUSINESS_PARTNER) |
| [List Business Partner Contacts](actions/list-business-partner-contacts.md) | `GET /A_BusinessPartner('{{businessPartner}}')/to_BusinessPartnerContact` | [docs](https://api.sap.com/api/API_BUSINESS_PARTNER) |
| [List Business Partner Data Controllers](actions/list-business-partner-data-controllers.md) | `GET /A_BusinessPartner('{{businessPartner}}')/to_BPDataController` | [docs](https://api.sap.com/api/API_BUSINESS_PARTNER) |
| [List Business Partner Employment Records](actions/list-business-partner-employment-records.md) | `GET /A_BusinessPartner('{{businessPartner}}')/to_BPEmployment` | [docs](https://api.sap.com/api/API_BUSINESS_PARTNER) |
| [List Business Partner Financial Reports](actions/list-business-partner-financial-reports.md) | `GET /A_BusinessPartner('{{businessPartner}}')/to_BPFinServicesReporting` | [docs](https://api.sap.com/api/API_BUSINESS_PARTNER) |
| [List Business Partner Fiscal Years](actions/list-business-partner-fiscal-years.md) | `GET /A_BusinessPartner('{{businessPartner}}')/to_BPFiscalYearInformation` | [docs](https://api.sap.com/api/API_BUSINESS_PARTNER) |
| [List Business Partner Identifications](actions/list-business-partner-identifications.md) | `GET /A_BusinessPartner('{{businessPartner}}')/to_BuPaIdentification` | [docs](https://api.sap.com/api/API_BUSINESS_PARTNER) |
| [List Business Partner Industries](actions/list-business-partner-industries.md) | `GET /A_BusinessPartner('{{businessPartner}}')/to_BuPaIndustry` | [docs](https://api.sap.com/api/API_BUSINESS_PARTNER) |
| [List Business Partner Ratings](actions/list-business-partner-ratings.md) | `GET /A_BusinessPartner('{{businessPartner}}')/to_BusinessPartnerRating` | [docs](https://api.sap.com/api/API_BUSINESS_PARTNER) |
| [List Business Partner Relationships](actions/list-business-partner-relationships.md) | `GET /A_BusinessPartner('{{businessPartner}}')/to_BPRelationship` | [docs](https://api.sap.com/api/API_BUSINESS_PARTNER) |
| [List Business Partner Roles](actions/list-business-partner-roles.md) | `GET /A_BusinessPartner('{{businessPartner}}')/to_BusinessPartnerRole` | [docs](https://api.sap.com/api/API_BUSINESS_PARTNER) |
| [List Business Partner Taxes](actions/list-business-partner-taxes.md) | `GET /A_BusinessPartner('{{businessPartner}}')/to_BusinessPartnerTax` | [docs](https://api.sap.com/api/API_BUSINESS_PARTNER) |
| [List Business Partners](actions/list-business-partners.md) | `GET /A_BusinessPartner` | [docs](https://api.sap.com/api/API_BUSINESS_PARTNER/resource/A_BusinessPartner) |
| [List Customer Companies](actions/list-customer-companies.md) | `GET /A_CustomerCompany` | [docs](https://api.sap.com/api/API_BUSINESS_PARTNER/resource/A_CustomerCompany) |
| [List Customer Sales Area Taxes](actions/list-customer-sales-area-taxes.md) | `GET /A_CustomerSalesAreaTax` | [docs](https://api.sap.com/api/API_BUSINESS_PARTNER/resource/A_CustomerSalesAreaTax) |
| [List Customer Sales Areas](actions/list-customer-sales-areas.md) | `GET /A_CustomerSalesArea` | [docs](https://api.sap.com/api/API_BUSINESS_PARTNER/resource/A_CustomerSalesArea) |
| [List Customer Sales Partner Functions](actions/list-customer-sales-partner-functions.md) | `GET /A_CustSalesPartnerFunc` | [docs](https://api.sap.com/api/API_BUSINESS_PARTNER/resource/A_CustSalesPartnerFunc) |
| [List Customers](actions/list-customers.md) | `GET /A_Customer` | [docs](https://api.sap.com/api/API_BUSINESS_PARTNER/resource/A_Customer) |
| [List Payment Cards](actions/list-payment-cards.md) | `GET /A_BusinessPartner('{{businessPartner}}')/to_PaymentCard` | [docs](https://api.sap.com/api/API_BUSINESS_PARTNER) |
| [List Supplier Companies](actions/list-supplier-companies.md) | `GET /A_SupplierCompany` | [docs](https://api.sap.com/api/API_BUSINESS_PARTNER/resource/A_SupplierCompany) |
| [List Supplier Partner Functions](actions/list-supplier-partner-functions.md) | `GET /A_SupplierPartnerFunc` | [docs](https://api.sap.com/api/API_BUSINESS_PARTNER/resource/A_SupplierPartnerFunc) |
| [List Supplier Purchasing Organizations](actions/list-supplier-purchasing-organizations.md) | `GET /A_SupplierPurchasingOrg` | [docs](https://api.sap.com/api/API_BUSINESS_PARTNER/resource/A_SupplierPurchasingOrg) |
| [List Supplier Withholding Taxes](actions/list-supplier-withholding-taxes.md) | `GET /A_SupplierWithHoldingTax` | [docs](https://api.sap.com/api/API_BUSINESS_PARTNER/resource/A_SupplierWithHoldingTax) |
| [List Suppliers](actions/list-suppliers.md) | `GET /A_Supplier` | [docs](https://api.sap.com/api/API_BUSINESS_PARTNER/resource/A_Supplier) |
