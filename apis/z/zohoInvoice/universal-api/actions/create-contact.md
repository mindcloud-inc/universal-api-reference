# Zoho Invoice: Create Contact

Creates a contact in Zoho Invoice.

```
POST https://connect.mindcloud.co/v1/universal/zohoInvoice/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Invoice `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoInvoice/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactName": "Acme Corp"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoInvoice/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactName": "Acme Corp"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactName` | string | yes | Name of the contact. This can be the name of an organisation or the name of an individual. Maximum length [200] Example: `Acme Corp`. |
| `companyName` | string | no | Name of the conact's company. Maximum length [200] Example: `Acme Corp`. |
| `paymentTerms` | number | no | Net payment term for the customer. Example: `30`. |
| `currencyId` | string | no | Currency ID of the customer's currency. Example: `460000000000097`. |
| `website` | string | no | Website of the contact. Example: `https://acme.example`. |
| `billingAddress` | object | no | Billing address of the contact. |
| `billingAddress.attention` | string | no | Attention of the contacts's billing address. Example: `Accounts Payable`. |
| `billingAddress.address` | string | no | Billing address of the contact. Maximum length allowed [500] Example: `123 Main St`. |
| `billingAddress.street2` | string | no | Example: `Suite 400`. |
| `billingAddress.stateCode` | string | no | Example: `CA`. |
| `billingAddress.city` | string | no | City of the customer's billing address. Example: `San Francisco`. |
| `billingAddress.state` | string | no | State of the customer's billing address. Example: `California`. |
| `billingAddress.zip` | string | no | Zip code of the customer's billing address. Example: `94105`. |
| `billingAddress.country` | string | no | Country of the customer's billing address. Example: `USA`. |
| `billingAddress.fax` | string | no | Customer's fax number. Example: `5551230000`. |
| `billingAddress.phone` | string | no | Phone number of the contact person. Example: `5551231234`. |
| `shippingAddress` | object | no | Customer's shipping address to which the goods must be delivered. |
| `shippingAddress.attention` | string | no | Attention of the contacts's billing address. Example: `Receiving`. |
| `shippingAddress.address` | string | no | Billing address of the contact. Maximum length allowed [500] Example: `500 Market St`. |
| `shippingAddress.street2` | string | no | Example: `Dock 3`. |
| `shippingAddress.stateCode` | string | no | Example: `CA`. |
| `shippingAddress.city` | string | no | City of the customer's billing address. Example: `San Francisco`. |
| `shippingAddress.state` | string | no | State of the customer's billing address. Example: `California`. |
| `shippingAddress.zip` | string | no | Zip code of the customer's billing address. Example: `94105`. |
| `shippingAddress.country` | string | no | Country of the customer's billing address. Example: `USA`. |
| `shippingAddress.fax` | string | no | Customer's fax number. Example: `5551230000`. |
| `shippingAddress.phone` | string | no | Phone number of the contact person. Example: `5551231234`. |
| `contactPersons[]` | array<object> | no | Person/Individual who represents a company |
| `contactPersons[].salutation` | string | no | Salutation for the contact Example: `Ms`. |
| `contactPersons[].firstName` | string | no | First name of the contact. Maximum length [100] Example: `Jane`. |
| `contactPersons[].lastName` | string | no | Last name of the contact. Maximum length [100] Example: `Doe`. |
| `contactPersons[].email` | string | no | The Email ID of the contact person. Example: `jane@example.com`. |
| `contactPersons[].phone` | string | no | Phone number of the contact person. Example: `5551231234`. |
| `contactPersons[].mobile` | string | no | Mobile number of the contact person. Example: `5551231234`. |
| `contactPersons[].isPrimaryContact` | boolean | no | To mark contact person as primary for contact. Allowed value is true only. |
| `notes` | string | no | Commennts about the payment made by the contact. Example: `Preferred customer`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customFields[]` | array<object> | no | Custom fields or additional fields for the contact. |
| `customFields[].value` | string | no | Value of the custom field. Example: `Preferred account`. |
| `customFields[].index` | number | no | Index of the custom field. It can hold any value from 1 to 10. Example: `1`. |
| `defaultTemplates` | object | no | ID of the Invoice template used |
| `defaultTemplates.invoiceTemplateId` | string | no | ID of the Invoice template used Example: `460000000012345`. |
| `defaultTemplates.invoiceTemplateName` | string | no | Name of the invoice template used Example: `Standard Invoice`. |
| `defaultTemplates.estimateTemplateId` | string | no | ID of the estimate template used Example: `460000000012346`. |
| `defaultTemplates.estimateTemplateName` | string | no | Name of the estimate template used Example: `Standard Estimate`. |
| `defaultTemplates.creditnoteTemplateId` | string | no | ID of teh credit note template used Example: `460000000012347`. |
| `defaultTemplates.creditnoteTemplateName` | string | no | Name of the credit note template used Example: `Standard Credit Note`. |
| `defaultTemplates.invoiceEmailTemplateId` | string | no | ID of the invoice email tempalte used Example: `460000000012348`. |
| `defaultTemplates.invoiceEmailTemplateName` | string | no | Name of the Invoice email template used Example: `Invoice Email`. |
| `defaultTemplates.estimateEmailTemplateId` | string | no | ID of the estimate email template used Example: `460000000012349`. |
| `defaultTemplates.estimateEmailTemplateName` | string | no | Name of the estimate email template used Example: `Estimate Email`. |
| `defaultTemplates.creditnoteEmailTemplateId` | string | no | ID of the credit note email template Example: `460000000012350`. |
| `defaultTemplates.creditnoteEmailTemplateName` | string | no | Name of the credit note email template Example: `Credit Note Email`. |
| `languageCode` | list<string> | no | language of a contact. allowed values de,en,es,fr,it,ja,nl,pt,sv,zh One of: `de`, `en`, `es`, `fr`, `it`, `ja`, `nl`, `pt`, `sv`, `zh`. Example: `en`. |
| `vatRegNo` | string | no | For UK Edition: VAT Registration number of a contact with length should be between 2 and 12 characters. For Avalara: If you are doing sales in the European Union (EU) then provide VAT Registration Number of your customers here. This is used to calculate VAT for B2B sales, from Avalara. Example: `GB123456789`. |
| `taxRegNo` | string | no | 12 digit Tax Registration number of a contact with Tax treatment as home_country_mexico , border_region_mexico , non_mexico . Consumers generic RFC: XAXX010101000 , Overseas generic RFC: XEXX010101000 Example: `RFC1234567890`. |
| `countryCode` | string | no | For UK Edition: Two letter country code of a contact For Avalara: Two letter country code for the customer country, if your customer is not in US. Refer [AvaTax Codes for Countries and States][2]. Example: `GB`. |
| `vatTreatment` | list<string> | no | VAT treatment of the contact.Allowed Values: uk (A business that is located in the UK.), eu_vat_registered (A business that is reg for VAT and trade goods between Northern Ireland and EU. This node is available only for organizations enabled for NI protocal in VAT Settings.) and overseas (A business that is located outside UK. Pre Brexit, this was split as eu_vat_registered , eu_vat_not_registered and non_eu ). One of: `eu_vat_registered`, `overseas`, `uk`. Example: `uk`. |
| `taxTreatment` | list<string> | no | VAT treatment of the contact.Allowed Values: home_country_mexico (A business that is located within MX) border_region_mexico (A business that is located in the northern and southern border regions in MX) non_mexico (A business that is located outside MX). One of: `border_region_mexico`, `home_country_mexico`, `non_mexico`. Example: `home_country_mexico`. |
| `taxRegime` | list<string> | no | Tax Regime of the contact.Allowed Values: general_legal_person , legal_entities_non_profit , resident_abroad , production_cooperative_societies , agricultural_livestock , optional_group_of_companies , coordinated , simplified_trust , wages_salaries_income , lease , property_disposal_acquisition , other_income , resident_abroad , divident_income , individual_business_professional , interest_income , income_obtaining_price , no_tax_obligation , tax_incorporation , income_through_technology_platform , simplified_trust . One of: `agricultural_livestock`, `coordinated`, `divident_income`, `general_legal_person`, `income_obtaining_price`, `income_through_technology_platform`, `individual_business_professional`, `interest_income`, `lease`, `legal_entities_non_profit`, `no_tax_obligation`, `optional_group_of_companies`, `other_income`, `production_cooperative_societies`, `property_disposal_acquisition`, `resident_abroad`, `simplified_trust`, `tax_incorporation`, `wages_salaries_income`. Example: `general_legal_person`. |
| `legalName` | string | no | Legal Name of the contact. Example: `Acme Ltd`. |
| `isTdsRegistered` | boolean | no | Boolean to check if tax is registered. |
| `placeOfContact` | string | no | Location of the contact. (This node identifies the place of supply and source of supply when invoices/bills are raised for the customer/vendor respectively. This is not applicable for Overseas contacts) Example: `TN`. |
| `gstNo` | string | no | 15 digit GST identification number of the customer/vendor. Example: `22AAAAA0000A1Z5`. |
| `gstTreatment` | list<string> | no | Choose whether the contact is GST registered/unregistered/consumer/overseas. Allowed values are business_gst , business_none , overseas , consumer . One of: `business_gst`, `business_none`, `consumer`, `overseas`. Example: `business_gst`. |
| `taxAuthorityName` | string | no | Enter tax authority name. Example: `California`. |
| `taxExemptionCode` | string | no | Enter tax exemption code Example: `EXEMPT`. |
| `avataxExemptNo` | string | no | Exemption certificate number of the customer. Example: `EX-12345`. |
| `avataxUseCode` | string | no | Used to group like customers for exemption purposes. It is a custom value that links customers to a tax rule. Select from Avalara [standard codes][1] or enter a custom code. Example: `A`. |
| `taxExemptionId` | string | no | ID of the tax exemption. Example: `460000000012351`. |
| `taxAuthorityId` | string | no | ID of the tax authority. Tax authority depends on the location of the customer. For example, if the customer is located in NY, then the tax authority is NY tax authority. Example: `460000000012352`. |
| `taxId` | string | no | ID of the tax or tax group that can be collected from the contact. Tax can be given only if is_taxable is true . Example: `460000000012353`. |
| `tdsTaxId` | string | no | ID of the TDS tax. Example: `460000000012354`. |
| `isTaxable` | boolean | no | Boolean to track the taxability of the customer. |
| `facebook` | string | no | Facebook profile account of the contact. Maximum length [100] Example: `acmeco`. |
| `twitter` | string | no | Twitter account of the contact. Maximum length [100] Example: `acmeco`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "companyName": "Ava Chen",
      "contactId": "string",
      "contactName": "Ava Chen",
      "contactType": "string",
      "createdTime": "2026-05-07T12:00:00.000Z",
      "currencyCode": "string",
      "customerName": "Ava Chen",
      "customerSubType": "string",
      "email": "ava@example.com",
      "hasAttachment": true,
      "lastModifiedTime": "2026-05-07T12:00:00.000Z",
      "mobile": "string",
      "phone": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companyName` | string |  |
| `contactId` | string |  |
| `contactName` | string |  |
| `contactType` | string |  |
| `createdTime` | date |  |
| `currencyCode` | string |  |
| `customerName` | string |  |
| `customerSubType` | string |  |
| `email` | string |  |
| `hasAttachment` | boolean |  |
| `lastModifiedTime` | date |  |
| `mobile` | string |  |
| `phone` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Zoho Invoice API, this operation is `POST /contacts` (base URL `https://www.zohoapis.com/invoice/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

