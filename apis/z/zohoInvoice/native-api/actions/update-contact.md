# Update Contact with Zoho Invoice

Updates a contact in Zoho Invoice.

## Endpoint

- **Method:** `PUT`
- **Path:** `/contacts/:contact_id`
- **Base URL:** `https://www.zohoapis.com/invoice/v3`
- **Official documentation:** [Update Contact](https://www.zoho.com/invoice/api/v3/contacts/#update-a-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_id` | path | `string` | yes | Unique identifier of the contact. |
| `contact_name` | body | `string` | yes | Name of the contact. This can be the name of an organisation or the name of an individual. Maximum length [200] Maximum length: 200. |
| `company_name` | body | `string` | no | Name of the conact's company. Maximum length [200] Maximum length: 200. |
| `payment_terms` | body | `number` | no | Net payment term for the customer. |
| `currency_id` | body | `string` | no | Currency ID of the customer's currency. |
| `website` | body | `string` | no | Website of the contact. |
| `custom_fields[]` | body | `array<object>` | no | Custom fields or Additional of the contact which we can create to add more information. |
| `custom_fields[].value` | body | `string` | no | Value of the custom field. |
| `custom_fields[].index` | body | `number` | no | Index of the custom field. It can hold any value from 1 to 10. |
| `custom_fields[].label` | body | `string` | no | Label of the custom field. |
| `billing_address` | body | `object` | no | Billing address of the contact. |
| `billing_address.attention` | body | `string` | no | Attention of the contacts's billing address. |
| `billing_address.address` | body | `string` | no | Billing address of the contact. Maximum length allowed [500] Maximum length: 500. |
| `billing_address.street2` | body | `string` | no | — |
| `billing_address.state_code` | body | `string` | no | — |
| `billing_address.city` | body | `string` | no | City of the customer's billing address. |
| `billing_address.state` | body | `string` | no | State of the customer's billing address. |
| `billing_address.zip` | body | `string` | no | Zip code of the customer's billing address. |
| `billing_address.country` | body | `string` | no | Country of the customer's billing address. |
| `billing_address.fax` | body | `string` | no | Customer's fax number. |
| `billing_address.phone` | body | `string` | no | Phone number of the contact person. |
| `shipping_address` | body | `object` | no | Customer's shipping address to which the goods must be delivered. |
| `shipping_address.attention` | body | `string` | no | Attention of the contacts's billing address. |
| `shipping_address.address` | body | `string` | no | Billing address of the contact. Maximum length allowed [500] Maximum length: 500. |
| `shipping_address.street2` | body | `string` | no | — |
| `shipping_address.state_code` | body | `string` | no | — |
| `shipping_address.city` | body | `string` | no | City of the customer's billing address. |
| `shipping_address.state` | body | `string` | no | State of the customer's billing address. |
| `shipping_address.zip` | body | `string` | no | Zip code of the customer's billing address. |
| `shipping_address.country` | body | `string` | no | Country of the customer's billing address. |
| `shipping_address.fax` | body | `string` | no | Customer's fax number. |
| `shipping_address.phone` | body | `string` | no | Phone number of the contact person. |
| `contact_persons[]` | body | `array<object>` | no | Person/Individual who represents a company |
| `contact_persons[].salutation` | body | `string` | no | Salutation for the contact |
| `contact_persons[].first_name` | body | `string` | no | First name of the contact. Maximum length [100] Maximum length: 100. |
| `contact_persons[].last_name` | body | `string` | no | Last name of the contact. Maximum length [100] Maximum length: 100. |
| `contact_persons[].email` | body | `string` | no | The Email ID of the contact person. |
| `contact_persons[].phone` | body | `string` | no | Phone number of the contact person. |
| `contact_persons[].mobile` | body | `string` | no | Mobile number of the contact person. |
| `contact_persons[].is_primary_contact` | body | `boolean` | no | To mark contact person as primary for contact. Allowed value is true only. |
| `default_templates` | body | `object` | no | ID of the Invoice template used |
| `default_templates.invoice_template_id` | body | `string` | no | ID of the Invoice template used |
| `default_templates.invoice_template_name` | body | `string` | no | Name of the invoice template used |
| `default_templates.estimate_template_id` | body | `string` | no | ID of the estimate template used |
| `default_templates.estimate_template_name` | body | `string` | no | Name of the estimate template used |
| `default_templates.creditnote_template_id` | body | `string` | no | ID of teh credit note template used |
| `default_templates.creditnote_template_name` | body | `string` | no | Name of the credit note template used |
| `default_templates.invoice_email_template_id` | body | `string` | no | ID of the invoice email tempalte used |
| `default_templates.invoice_email_template_name` | body | `string` | no | Name of the Invoice email template used |
| `default_templates.estimate_email_template_id` | body | `string` | no | ID of the estimate email template used |
| `default_templates.estimate_email_template_name` | body | `string` | no | Name of the estimate email template used |
| `default_templates.creditnote_email_template_id` | body | `string` | no | ID of the credit note email template |
| `default_templates.creditnote_email_template_name` | body | `string` | no | Name of the credit note email template |
| `language_code` | body | `list<string>` | no | language of a contact. allowed values de,en,es,fr,it,ja,nl,pt,sv,zh Accepted values: `de`, `en`, `es`, `fr`, `it`, `ja`, `nl`, `pt`, `sv`, `zh`. |
| `notes` | body | `string` | no | Commennts about the payment made by the contact. |
| `vat_reg_no` | body | `string` | no | For UK Edition: VAT Registration number of a contact with length should be between 2 and 12 characters. For Avalara: If you are doing sales in the European Union (EU) then provide VAT Registration Number of your customers here. This is used to calculate VAT for B2B sales, from Avalara. |
| `tax_reg_no` | body | `string` | no | 12 digit Tax Registration number of a contact with Tax treatment as home_country_mexico , border_region_mexico , non_mexico . Consumers generic RFC: XAXX010101000 , Overseas generic RFC: XEXX010101000 |
| `country_code` | body | `string` | no | For UK Edition: Two letter country code of a contact For Avalara: Two letter country code for the customer country, if your customer is not in US. Refer [AvaTax Codes for Countries and States][2]. |
| `vat_treatment` | body | `list<string>` | no | VAT treatment of the contact.Allowed Values: uk (A business that is located in the UK.), eu_vat_registered (A business that is reg for VAT and trade goods between Northern Ireland and EU. This node is available only for organizations enabled for NI protocal in VAT Settings.) and overseas (A business that is located outside UK. Pre Brexit, this was split as eu_vat_registered , eu_vat_not_registered and non_eu ). Accepted values: `eu_vat_registered`, `overseas`, `uk`. |
| `tax_treatment` | body | `list<string>` | no | VAT treatment of the contact.Allowed Values: home_country_mexico (A business that is located within MX) border_region_mexico (A business that is located in the northern and southern border regions in MX) non_mexico (A business that is located outside MX). Accepted values: `border_region_mexico`, `home_country_mexico`, `non_mexico`. |
| `tax_regime` | body | `list<string>` | no | Tax Regime of the contact.Allowed Values: general_legal_person , legal_entities_non_profit , resident_abroad , production_cooperative_societies , agricultural_livestock , optional_group_of_companies , coordinated , simplified_trust , wages_salaries_income , lease , property_disposal_acquisition , other_income , resident_abroad , divident_income , individual_business_professional , interest_income , income_obtaining_price , no_tax_obligation , tax_incorporation , income_through_technology_platform , simplified_trust . Accepted values: `agricultural_livestock`, `coordinated`, `divident_income`, `general_legal_person`, `income_obtaining_price`, `income_through_technology_platform`, `individual_business_professional`, `interest_income`, `lease`, `legal_entities_non_profit`, `no_tax_obligation`, `optional_group_of_companies`, `other_income`, `production_cooperative_societies`, `property_disposal_acquisition`, `resident_abroad`, `simplified_trust`, `tax_incorporation`, `wages_salaries_income`. |
| `legal_name` | body | `string` | no | Legal Name of the contact. |
| `is_tds_registered` | body | `boolean` | no | Boolean to check if tax is registered. |
| `place_of_contact` | body | `string` | no | Location of the contact. (This node identifies the place of supply and source of supply when invoices/bills are raised for the customer/vendor respectively. This is not applicable for Overseas contacts) |
| `gst_no` | body | `string` | no | 15 digit GST identification number of the customer/vendor. |
| `gst_treatment` | body | `list<string>` | no | Choose whether the contact is GST registered/unregistered/consumer/overseas. Allowed values are business_gst , business_none , overseas , consumer . Accepted values: `business_gst`, `business_none`, `consumer`, `overseas`. |
| `tax_authority_name` | body | `string` | no | Enter tax authority name. |
| `tax_exemption_code` | body | `string` | no | Enter tax exemption code |
| `avatax_exempt_no` | body | `string` | no | Exemption certificate number of the customer. |
| `avatax_use_code` | body | `string` | no | Used to group like customers for exemption purposes. It is a custom value that links customers to a tax rule. Select from Avalara [standard codes][1] or enter a custom code. |
| `tax_exemption_id` | body | `string` | no | ID of the tax exemption. |
| `tax_authority_id` | body | `string` | no | ID of the tax authority. Tax authority depends on the location of the customer. For example, if the customer is located in NY, then the tax authority is NY tax authority. |
| `tax_id` | body | `string` | no | ID of the tax or tax group that can be collected from the contact. Tax can be given only if is_taxable is true . |
| `tds_tax_id` | body | `string` | no | ID of the TDS tax. |
| `is_taxable` | body | `boolean` | no | Boolean to track the taxability of the customer. |
| `facebook` | body | `string` | no | Facebook profile account of the contact. Maximum length [100] Maximum length: 100. |
| `twitter` | body | `string` | no | Twitter account of the contact. Maximum length [100] Maximum length: 100. |
