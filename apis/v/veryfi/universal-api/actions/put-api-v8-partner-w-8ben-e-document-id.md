# Veryfi: Update a W-8BEN-E

Updates an existing W-8BEN-E in Veryfi.

```
PUT https://connect.mindcloud.co/v1/universal/veryfi/latest/actions/put-api-v8-partner-w-8ben-e-document-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Veryfi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/veryfi/latest/actions/put-api-v8-partner-w-8ben-e-document-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "documentId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/veryfi/latest/actions/put-api-v8-partner-w-8ben-e-document-id', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "documentId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `documentId` | string | yes |  |
| `externalId` | string | no | Possible values: non-empty Deprecated 2025-01-09, use meta.external_id instead. |
| `meta` | string | no | Possible values: non-empty Possible values: non-empty Default value: `` |

## Response

```json
{
  "success": true,
  "data": [
    {
      "certify_checkbox": {},
      "created_date": "string",
      "external_id": "string",
      "field_1_name": {},
      "field_10_reference_number": {},
      "field_11_checkbox_branch_nonparticipating_ffi": {},
      "field_11_checkbox_participating_ffi": {},
      "field_11_checkbox_reporting_model_one_ffi": {},
      "field_11_checkbox_reporting_model_two_ffi": {},
      "field_11_checkbox_us_branch": {},
      "field_12_disregarded_entity_city": {},
      "field_12_disregarded_entity_country": {},
      "field_12_disregarded_entity_street": {},
      "field_13_disregarded_entity_giin": {},
      "field_14a_checkbox": {},
      "field_14a_resident_of": {},
      "field_14b_checkbox_active_trade_or_business_test": {},
      "field_14b_checkbox_benefit_items": {},
      "field_14b_checkbox_derivative_benefits_test": {},
      "field_14b_checkbox_favorable": {},
      "field_14b_checkbox_government": {},
      "field_14b_checkbox_no_lob_article_in_treaty": {},
      "field_14b_checkbox_other": {},
      "field_14b_checkbox_other_tax_exempt": {},
      "field_14b_checkbox_ownership_and_base_erosion_test": {},
      "field_14b_checkbox_publicly_traded_corporation": {},
      "field_14b_checkbox_subsidiary_of_publicly_traded_corporation": {},
      "field_14b_checkbox_tax_exempt_pension": {},
      "field_14b_other_article": {},
      "field_14c_checkbox_dividends": {},
      "field_15_special_rates_article": {},
      "field_15_special_rates_explanation": {},
      "field_15_special_rates_income_type": {},
      "field_15_special_rates_percentage": {},
      "field_16_name": {},
      "field_17a_checkbox": {},
      "field_17b_checkbox": {},
      "field_18_checkbox": {},
      "field_19_checkbox": {},
      "field_2_country": {},
      "field_20_name": {},
      "field_21_checkbox": {},
      "field_22_checkbox": {},
      "field_23_checkbox": {},
      "field_24a_checkbox": {},
      "field_24b_checkbox": {},
      "field_24c_checkbox": {},
      "field_24d_checkbox": {},
      "field_25a_checkbox": {},
      "field_25b_checkbox": {},
      "field_25c_checkbox": {},
      "field_26_checkbox": {},
      "field_26_checkbox_model_one": {},
      "field_26_checkbox_model_two": {},
      "field_26_checkbox_trustee_foreign": {},
      "field_26_checkbox_trustee_us": {},
      "field_26_country": {},
      "field_26_treated_as": {},
      "field_26_trustee_name": {},
      "field_27_checkbox": {},
      "field_28a_checkbox": {},
      "field_28b_checkbox": {},
      "field_29a_checkbox": {},
      "field_29b_checkbox": {},
      "field_29c_checkbox": {},
      "field_29d_checkbox": {},
      "field_29e_checkbox": {},
      "field_29f_checkbox": {},
      "field_3_disregarded_entity_name": {},
      "field_30_checkbox": {},
      "field_31_checkbox": {},
      "field_32_checkbox": {},
      "field_33_checkbox": {},
      "field_33_date": {},
      "field_34_checkbox": {},
      "field_34_date": {},
      "field_35_checkbox": {},
      "field_35_date": {},
      "field_36_checkbox": {},
      "field_37a_checkbox": {},
      "field_37a_name": {},
      "field_37b_checkbox": {},
      "field_37b_market_name": {},
      "field_37b_name": {},
      "field_38_checkbox": {},
      "field_39_checkbox": {},
      "field_4_checkbox_central_issue_bank": {},
      "field_4_checkbox_complex_trust": {},
      "field_4_checkbox_corporation": {},
      "field_4_checkbox_disregarded_entity": {},
      "field_4_checkbox_estate": {},
      "field_4_checkbox_foreign_government_controlled_entity": {},
      "field_4_checkbox_foreign_government_integral_part": {},
      "field_4_checkbox_grantor_trust": {},
      "field_4_checkbox_hybrid_no": {},
      "field_4_checkbox_hybrid_yes": {},
      "field_4_checkbox_international_organization": {},
      "field_4_checkbox_partnership": {},
      "field_4_checkbox_private_foundation": {},
      "field_4_checkbox_simple_trust": {},
      "field_4_checkbox_tax_exempt_organization": {},
      "field_40a_checkbox": {},
      "field_40b_checkbox": {},
      "field_40c_checkbox": {},
      "field_41_checkbox": {},
      "field_42_name": {},
      "field_43_checkbox": {},
      "field_5_checkbox_active_nffe": {},
      "field_5_checkbox_certain_investment_entities_that_do_not_maintain_financial_accounts": {},
      "field_5_checkbox_certified_deemed_compliant_ffi_low_value_accounts": {},
      "field_5_checkbox_certified_deemed_compliant_limited_life_debt_investment_entity": {},
      "field_5_checkbox_certified_deemed_compliant_nonregistering_local_bank": {},
      "field_5_checkbox_certified_deemed_compliant_sponsored_closely_held_investment_vehicle": {},
      "field_5_checkbox_direct_reporting_nffe": {},
      "field_5_checkbox_entity_wholly_owned_exempt": {},
      "field_5_checkbox_excepted_inter_affiliate_ffi": {},
      "field_5_checkbox_excepted_nonfiancial_entity_bankruptcy": {},
      "field_5_checkbox_excepted_nonfiancial_group_entity": {},
      "field_5_checkbox_excepted_nonfiancial_start_up": {},
      "field_5_checkbox_excepted_territory_nffe": {},
      "field_5_checkbox_exempt_retirement_plans": {},
      "field_5_checkbox_foreign_government": {},
      "field_5_checkbox_international_organization": {},
      "field_5_checkbox_nonparticipating_ffi": {},
      "field_5_checkbox_nonprofit": {},
      "field_5_checkbox_nonreporting_iga_ffi": {},
      "field_5_checkbox_not_financial_account": {},
      "field_5_checkbox_organization_501c": {},
      "field_5_checkbox_owner_documented_ffi": {},
      "field_5_checkbox_participating_ffi": {},
      "field_5_checkbox_passive_nffe": {},
      "field_5_checkbox_publicly_traded_nffe": {},
      "field_5_checkbox_registered_deemed_compliant_ffi": {},
      "field_5_checkbox_reporting_model_one_ffi": {},
      "field_5_checkbox_reporting_model_two_ffi": {},
      "field_5_checkbox_restricted_distributor": {},
      "field_5_checkbox_sponsored_direct_reporting_nffe": {},
      "field_5_checkbox_sponsored_ffi": {},
      "field_5_checkbox_territory_financial_institutions": {},
      "field_6_address": {},
      "field_6_city": {},
      "field_6_country": {},
      "field_7_mailing_city": {},
      "field_7_mailing_country": {},
      "field_7_mailing_street": {},
      "field_8_tin": {},
      "field_9a_giin": {},
      "field_9b_foreign_tin": {},
      "field_9c_checkbox_tin_not_required": {},
      "id": 1,
      "img_thumbnail_url": "https://example.com",
      "meta": {},
      "passive_nffe_owners": [
        {}
      ],
      "pdf_url": "https://example.com",
      "signature_date": {},
      "signature_name": {},
      "signed": {},
      "updated_date": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `certify_checkbox` | object |  |
| `created_date` | string |  |
| `external_id` | string |  |
| `field_1_name` | object |  |
| `field_10_reference_number` | object |  |
| `field_11_checkbox_branch_nonparticipating_ffi` | object |  |
| `field_11_checkbox_participating_ffi` | object |  |
| `field_11_checkbox_reporting_model_one_ffi` | object |  |
| `field_11_checkbox_reporting_model_two_ffi` | object |  |
| `field_11_checkbox_us_branch` | object |  |
| `field_12_disregarded_entity_city` | object |  |
| `field_12_disregarded_entity_country` | object |  |
| `field_12_disregarded_entity_street` | object |  |
| `field_13_disregarded_entity_giin` | object |  |
| `field_14a_checkbox` | object |  |
| `field_14a_resident_of` | object |  |
| `field_14b_checkbox_active_trade_or_business_test` | object |  |
| `field_14b_checkbox_benefit_items` | object |  |
| `field_14b_checkbox_derivative_benefits_test` | object |  |
| `field_14b_checkbox_favorable` | object |  |
| `field_14b_checkbox_government` | object |  |
| `field_14b_checkbox_no_lob_article_in_treaty` | object |  |
| `field_14b_checkbox_other` | object |  |
| `field_14b_checkbox_other_tax_exempt` | object |  |
| `field_14b_checkbox_ownership_and_base_erosion_test` | object |  |
| `field_14b_checkbox_publicly_traded_corporation` | object |  |
| `field_14b_checkbox_subsidiary_of_publicly_traded_corporation` | object |  |
| `field_14b_checkbox_tax_exempt_pension` | object |  |
| `field_14b_other_article` | object |  |
| `field_14c_checkbox_dividends` | object |  |
| `field_15_special_rates_article` | object |  |
| `field_15_special_rates_explanation` | object |  |
| `field_15_special_rates_income_type` | object |  |
| `field_15_special_rates_percentage` | object |  |
| `field_16_name` | object |  |
| `field_17a_checkbox` | object |  |
| `field_17b_checkbox` | object |  |
| `field_18_checkbox` | object |  |
| `field_19_checkbox` | object |  |
| `field_2_country` | object |  |
| `field_20_name` | object |  |
| `field_21_checkbox` | object |  |
| `field_22_checkbox` | object |  |
| `field_23_checkbox` | object |  |
| `field_24a_checkbox` | object |  |
| `field_24b_checkbox` | object |  |
| `field_24c_checkbox` | object |  |
| `field_24d_checkbox` | object |  |
| `field_25a_checkbox` | object |  |
| `field_25b_checkbox` | object |  |
| `field_25c_checkbox` | object |  |
| `field_26_checkbox` | object |  |
| `field_26_checkbox_model_one` | object |  |
| `field_26_checkbox_model_two` | object |  |
| `field_26_checkbox_trustee_foreign` | object |  |
| `field_26_checkbox_trustee_us` | object |  |
| `field_26_country` | object |  |
| `field_26_treated_as` | object |  |
| `field_26_trustee_name` | object |  |
| `field_27_checkbox` | object |  |
| `field_28a_checkbox` | object |  |
| `field_28b_checkbox` | object |  |
| `field_29a_checkbox` | object |  |
| `field_29b_checkbox` | object |  |
| `field_29c_checkbox` | object |  |
| `field_29d_checkbox` | object |  |
| `field_29e_checkbox` | object |  |
| `field_29f_checkbox` | object |  |
| `field_3_disregarded_entity_name` | object |  |
| `field_30_checkbox` | object |  |
| `field_31_checkbox` | object |  |
| `field_32_checkbox` | object |  |
| `field_33_checkbox` | object |  |
| `field_33_date` | object |  |
| `field_34_checkbox` | object |  |
| `field_34_date` | object |  |
| `field_35_checkbox` | object |  |
| `field_35_date` | object |  |
| `field_36_checkbox` | object |  |
| `field_37a_checkbox` | object |  |
| `field_37a_name` | object |  |
| `field_37b_checkbox` | object |  |
| `field_37b_market_name` | object |  |
| `field_37b_name` | object |  |
| `field_38_checkbox` | object |  |
| `field_39_checkbox` | object |  |
| `field_4_checkbox_central_issue_bank` | object |  |
| `field_4_checkbox_complex_trust` | object |  |
| `field_4_checkbox_corporation` | object |  |
| `field_4_checkbox_disregarded_entity` | object |  |
| `field_4_checkbox_estate` | object |  |
| `field_4_checkbox_foreign_government_controlled_entity` | object |  |
| `field_4_checkbox_foreign_government_integral_part` | object |  |
| `field_4_checkbox_grantor_trust` | object |  |
| `field_4_checkbox_hybrid_no` | object |  |
| `field_4_checkbox_hybrid_yes` | object |  |
| `field_4_checkbox_international_organization` | object |  |
| `field_4_checkbox_partnership` | object |  |
| `field_4_checkbox_private_foundation` | object |  |
| `field_4_checkbox_simple_trust` | object |  |
| `field_4_checkbox_tax_exempt_organization` | object |  |
| `field_40a_checkbox` | object |  |
| `field_40b_checkbox` | object |  |
| `field_40c_checkbox` | object |  |
| `field_41_checkbox` | object |  |
| `field_42_name` | object |  |
| `field_43_checkbox` | object |  |
| `field_5_checkbox_active_nffe` | object |  |
| `field_5_checkbox_certain_investment_entities_that_do_not_maintain_financial_accounts` | object |  |
| `field_5_checkbox_certified_deemed_compliant_ffi_low_value_accounts` | object |  |
| `field_5_checkbox_certified_deemed_compliant_limited_life_debt_investment_entity` | object |  |
| `field_5_checkbox_certified_deemed_compliant_nonregistering_local_bank` | object |  |
| `field_5_checkbox_certified_deemed_compliant_sponsored_closely_held_investment_vehicle` | object |  |
| `field_5_checkbox_direct_reporting_nffe` | object |  |
| `field_5_checkbox_entity_wholly_owned_exempt` | object |  |
| `field_5_checkbox_excepted_inter_affiliate_ffi` | object |  |
| `field_5_checkbox_excepted_nonfiancial_entity_bankruptcy` | object |  |
| `field_5_checkbox_excepted_nonfiancial_group_entity` | object |  |
| `field_5_checkbox_excepted_nonfiancial_start_up` | object |  |
| `field_5_checkbox_excepted_territory_nffe` | object |  |
| `field_5_checkbox_exempt_retirement_plans` | object |  |
| `field_5_checkbox_foreign_government` | object |  |
| `field_5_checkbox_international_organization` | object |  |
| `field_5_checkbox_nonparticipating_ffi` | object |  |
| `field_5_checkbox_nonprofit` | object |  |
| `field_5_checkbox_nonreporting_iga_ffi` | object |  |
| `field_5_checkbox_not_financial_account` | object |  |
| `field_5_checkbox_organization_501c` | object |  |
| `field_5_checkbox_owner_documented_ffi` | object |  |
| `field_5_checkbox_participating_ffi` | object |  |
| `field_5_checkbox_passive_nffe` | object |  |
| `field_5_checkbox_publicly_traded_nffe` | object |  |
| `field_5_checkbox_registered_deemed_compliant_ffi` | object |  |
| `field_5_checkbox_reporting_model_one_ffi` | object |  |
| `field_5_checkbox_reporting_model_two_ffi` | object |  |
| `field_5_checkbox_restricted_distributor` | object |  |
| `field_5_checkbox_sponsored_direct_reporting_nffe` | object |  |
| `field_5_checkbox_sponsored_ffi` | object |  |
| `field_5_checkbox_territory_financial_institutions` | object |  |
| `field_6_address` | object |  |
| `field_6_city` | object |  |
| `field_6_country` | object |  |
| `field_7_mailing_city` | object |  |
| `field_7_mailing_country` | object |  |
| `field_7_mailing_street` | object |  |
| `field_8_tin` | object |  |
| `field_9a_giin` | object |  |
| `field_9b_foreign_tin` | object |  |
| `field_9c_checkbox_tin_not_required` | object |  |
| `id` | number |  |
| `img_thumbnail_url` | string |  |
| `meta` | object |  |
| `passive_nffe_owners` | array<object> |  |
| `pdf_url` | string |  |
| `signature_date` | object |  |
| `signature_name` | object |  |
| `signed` | object |  |
| `updated_date` | string |  |

## Native endpoint

Through the native Veryfi API, this operation is `PUT /api/v8/partner/w-8ben-e/:document_id` (base URL `https://api.veryfi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/put-api-v8-partner-w-8ben-e-document-id.md) for the provider-specific parameters and requirements.

