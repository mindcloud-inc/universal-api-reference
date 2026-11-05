# Search AR Objects with Viewpoint Vista

Search objects found in the Viewpoint® Vista™ Accounts Receivable (AR) programs.

## Endpoint

- **Method:** `POST`
- **Path:** `v1/direct/subscribers/:subscriber_code/vista/:api/2/data/:object/cache/search`
- **Base URL:** `https://api.xchange.trimble.com/connect/`
- **API:** REST
- **Official documentation:** [Search AR Objects](https://direct-api.xchange.trimble.com/reference/get-directsubscriberssubscriber_codevistasm2datacustomerscache)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `modifiedUtcAfter` | body | `date` | no | — |
| `modifiedUtcBefore` | body | `date` | no | — |
| `object` | path | `list<string>` | yes | Specify the type of Object from the Accounts Receivable V2 Direct API that you'd like to retrieve. Accepted values: `batch_entries`, `batch_entry_lines`, `batches`, `company_parameters`, `credit_notes`, `customers`, `distribution_codes`, `receivable_types`, `transaction_lines`, `transactions`. |
| `rawFilters[]` | body | `array<object>` | no | Array of Trimble filters, combined with AND. Each item: { "propertyName": "Customer", "operator": "Equal", "value": 10009 }. The value's JSON type must match the property (number for integer fields like Customer/CustGroup, string for text, true/false for booleans, array for In). Operators: Equal, NotEqual, GreaterThan, GreaterThanOrEqual, LessThan, LessThanOrEqual, Like, StartsWith, EndsWith, Contains (strings only), In (array value). Dot-notation is supported for nested properties. |
