# <img src="https://images.mindcloud.co/apps/icons/sapcom_1775842136492.png" alt="SAP ERP (S/4HANA) logo" width="28" height="28"> SAP ERP (S/4HANA): Universal API

Create, read, update, or delete business partner, supplier, and customer master data in SAP S/4HANA Cloud Public Edition through the Business Partner (A2X) sandbox API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/sAPERPS4HANA/latest
- **Category:** Commerce / ERP
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.sap.com/products/erp/s4hana.html
- **Vendor API docs:** https://api.sap.com/api/API_BUSINESS_PARTNER/overview

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Business Partners](actions/list-business-partners.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sAPERPS4HANA/latest/actions/list-business-partners?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [List Address Independent Emails](actions/list-address-independent-emails.md) | GET | Retrieves address-independent emails from SAP ERP (S/4HANA). |
| [List Address Independent Faxes](actions/list-address-independent-faxes.md) | GET | Retrieves address-independent faxes from SAP ERP (S/4HANA). |
| [List Address Independent Mobiles](actions/list-address-independent-mobiles.md) | GET | Retrieves address-independent mobiles from SAP ERP (S/4HANA). |
| [List Address Independent Phones](actions/list-address-independent-phones.md) | GET | Retrieves address-independent phones from SAP ERP (S/4HANA). |
| [List Address Independent Websites](actions/list-address-independent-websites.md) | GET | Retrieves address-independent websites from SAP ERP (S/4HANA). |
| [List Business Partner Address Emails](actions/list-business-partner-address-emails.md) | GET | Retrieves business partner address emails from SAP ERP (S/4HANA). |
| [List Business Partner Address Phones](actions/list-business-partner-address-phones.md) | GET | Retrieves business partner address phones from SAP ERP (S/4HANA). |
| [List Business Partner Contacts](actions/list-business-partner-contacts.md) | GET | Retrieves contacts for a business partner from SAP ERP (S/4HANA). |

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [List Customer Companies](actions/list-customer-companies.md) | GET | Retrieves customer companies from SAP ERP (S/4HANA). |
| [List Customer Sales Area Taxes](actions/list-customer-sales-area-taxes.md) | GET | Retrieves customer sales area taxes from SAP ERP (S/4HANA). |
| [List Customer Sales Areas](actions/list-customer-sales-areas.md) | GET | Retrieves customer sales areas from SAP ERP (S/4HANA). |
| [List Customer Sales Partner Functions](actions/list-customer-sales-partner-functions.md) | GET | Retrieves customer sales partner functions from SAP ERP (S/4HANA). |
| [List Customers](actions/list-customers.md) | GET | Retrieves customers from SAP ERP (S/4HANA). |

### Organizations

| Action | Method | Description |
| --- | --- | --- |
| [Get Business Partner](actions/get-business-partner.md) | GET | Retrieves a business partner from SAP ERP (S/4HANA). |
| [Get Business Partner Bank Profile](actions/get-business-partner-bank-profile.md) | GET | Retrieves a business partner bank profile from SAP ERP (S/4HANA). |
| [Get Business Partner Credit Worthiness](actions/get-business-partner-credit-worthiness.md) | GET | Retrieves credit worthiness for a business partner from SAP ERP (S/4HANA). |
| [Get Customer for Business Partner](actions/get-customer-for-business-partner.md) | GET | Retrieves the customer for a business partner from SAP ERP (S/4HANA). |
| [Get Related Business Partner](actions/get-related-business-partner.md) | GET | Retrieves a related business partner from SAP ERP (S/4HANA). |
| [Get Supplier for Business Partner](actions/get-supplier-for-business-partner.md) | GET | Retrieves the supplier for a business partner from SAP ERP (S/4HANA). |
| [List Address-Dependent Tax Numbers](actions/list-address-dependent-tax-numbers.md) | GET | Retrieves address-dependent tax numbers from SAP ERP (S/4HANA). |
| [List Business Partner Addresses](actions/list-business-partner-addresses.md) | GET | Retrieves addresses for a business partner from SAP ERP (S/4HANA). |
| [List Business Partner Aliases](actions/list-business-partner-aliases.md) | GET | Retrieves aliases for a business partner from SAP ERP (S/4HANA). |
| [List Business Partner Banks](actions/list-business-partner-banks.md) | GET | Retrieves banks for a business partner from SAP ERP (S/4HANA). |
| [List Business Partner Data Controllers](actions/list-business-partner-data-controllers.md) | GET | Retrieves data controllers for a business partner from SAP ERP (S/4HANA). |
| [List Business Partner Employment Records](actions/list-business-partner-employment-records.md) | GET | Retrieves employment records for a business partner from SAP ERP (S/4HANA). |
| [List Business Partner Financial Reports](actions/list-business-partner-financial-reports.md) | GET | Retrieves financial reports for a business partner from SAP ERP (S/4HANA). |
| [List Business Partner Fiscal Years](actions/list-business-partner-fiscal-years.md) | GET | Retrieves fiscal years for a business partner from SAP ERP (S/4HANA). |
| [List Business Partner Identifications](actions/list-business-partner-identifications.md) | GET | Retrieves identifications for a business partner from SAP ERP (S/4HANA). |
| [List Business Partner Industries](actions/list-business-partner-industries.md) | GET | Retrieves industries for a business partner from SAP ERP (S/4HANA). |
| [List Business Partner Ratings](actions/list-business-partner-ratings.md) | GET | Retrieves ratings for a business partner from SAP ERP (S/4HANA). |
| [List Business Partner Relationships](actions/list-business-partner-relationships.md) | GET | Retrieves relationships for a business partner from SAP ERP (S/4HANA). |
| [List Business Partner Roles](actions/list-business-partner-roles.md) | GET | Retrieves roles for a business partner from SAP ERP (S/4HANA). |
| [List Business Partner Taxes](actions/list-business-partner-taxes.md) | GET | Retrieves taxes for a business partner from SAP ERP (S/4HANA). |
| [List Business Partners](actions/list-business-partners.md) | GET | Retrieves business partners from SAP ERP (S/4HANA). |
| [List Payment Cards](actions/list-payment-cards.md) | GET | Retrieves payment cards for a business partner from SAP ERP (S/4HANA). |

### Vendors

| Action | Method | Description |
| --- | --- | --- |
| [List Supplier Companies](actions/list-supplier-companies.md) | GET | Retrieves supplier companies from SAP ERP (S/4HANA). |
| [List Supplier Partner Functions](actions/list-supplier-partner-functions.md) | GET | Retrieves supplier partner functions from SAP ERP (S/4HANA). |
| [List Supplier Purchasing Organizations](actions/list-supplier-purchasing-organizations.md) | GET | Retrieves supplier purchasing organizations from SAP ERP (S/4HANA). |
| [List Supplier Withholding Taxes](actions/list-supplier-withholding-taxes.md) | GET | Retrieves supplier withholding taxes from SAP ERP (S/4HANA). |
| [List Suppliers](actions/list-suppliers.md) | GET | Retrieves suppliers from SAP ERP (S/4HANA). |

