# Search JC Objects with Viewpoint Vista

Search objects found in Viewpoint® Vista™ Job Cost (JC) programs.

## Endpoint

- **Method:** `POST`
- **Path:** `v1/direct/subscribers/:subscriber_code/vista/:api/2/data/:object/cache/search`
- **Base URL:** `https://api.xchange.trimble.com/connect/`
- **API:** REST
- **Official documentation:** [Search JC Objects](https://direct-api.xchange.trimble.com/reference/get-directsubscriberssubscriber_codevistasm2datacustomerscache)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `modifiedUtcAfter` | body | `date` | no | — |
| `object` | path | `list<string>` | yes | Specify the type of Object from the Job Cost V2 Direct API that you'd like to retrieve. Accepted values: `budget_codes`, `change_orders`, `company_parameters`, `contract_cls_batches`, `contract_cls_entries`, `contract_headers`, `contract_items`, `contracts`, `cost_adj_bat_entries`, `cost_adj_batches`, `cost_detail`, `cost_detail_period`, `cost_types`, `departments`, `field_tickets`, `fixed_rate_templates`, `insurance_templates`, `job_costs`, `job_phases`, `jobs`, `liability_templates`, `mat_use_bat_entries`, `mat_use_batches`, `metric_conversions`, `original_estimates`, `phases`, `progress_bat_entries`, `progress_batches`, `proj_bat_entries`, `proj_batches`, `project_managers`, `projection_notes`, `std_item_codes`. |
| `modifiedUtcBefore` | body | `date` | no | — |
