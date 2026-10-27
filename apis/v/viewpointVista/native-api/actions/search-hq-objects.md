# Search HQ Objects with Viewpoint Vista

Search objects found in Viewpoint® Vista™ Headquarters (HQ) programs.

## Endpoint

- **Method:** `POST`
- **Path:** `v1/direct/subscribers/:subscriber_code/vista/:api/2/data/:object/cache/search`
- **Base URL:** `https://api.xchange.trimble.com/connect/`
- **API:** REST
- **Official documentation:** [Search HQ Objects](https://direct-api.xchange.trimble.com/reference/get-directsubscriberssubscriber_codevistasm2datacustomerscache)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `modifiedUtcAfter` | body | `date` | no | — |
| `object` | path | `list<string>` | yes | Specify the type of Object from the Headquarters V2 Direct API that you'd like to retrieve. Accepted values: `company_parameters`, `compliance_codes`, `compliance_groups`, `contacts`, `countries`, `earn_types`, `escalation_indexes`, `escalation_materials`, `frequency_codes`, `groups`, `hold_codes`, `insurance_codes`, `liability_types`, `material_categories`, `materials`, `payment_terms`, `project_statuses`, `reason_codes`, `reviewer_groups`, `reviewers`, `roles`, `smsa_codes`, `standard_notes`, `tax_codes`, `unit_of_measures`. |
| `modifiedUtcBefore` | body | `date` | no | — |
