# Search AR Objects with Viewpoint Vista

Search objects found in the Viewpoint® Vista™ Accounts Receivable (AR) programs.

## Endpoint

- **Method:** `POST`
- **Path:** `v1/direct/subscribers/:subscriber_code/vista/:api/2/data/:object/cache/search`
- **Base URL:** `https://api.xchange.trimble.com/connect/`
- **API:** REST
- **Official documentation:** [Search AR Objects](https://direct-api.xchange.trimble.com/reference/post-directsubscriberssubscriber_codevistasm2datacustomerscachesearchsearch)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `modifiedUtcAfter` | body | `date` | no | — |
| `rawFilters[].propertyName` | body | `string` | no | Property of the object to filter on, exactly as Trimble returns it (case-sensitive), e.g. Customer, Name, CustGroup. Dot-notation works for nested properties (e.g. __custom_fields.udServiceTitanId), but not for properties inside arrays. |
| `modifiedUtcBefore` | body | `date` | no | — |
| `rawFilters[].operator` | body | `list<string>` | no | Comparison operator. Like, StartsWith, EndsWith and Contains work only on text values. In needs a list value. Accepted values: `Contains`, `EndsWith`, `Equal`, `GreaterThan`, `GreaterThanOrEqual`, `In`, `LessThan`, `LessThanOrEqual`, `Like`, `NotEqual`, `StartsWith`. |
| `object` | path | `list<string>` | yes | Specify the type of Object from the Accounts Receivable V2 Direct API that you'd like to retrieve. Accepted values: `batch_entries`, `batch_entry_lines`, `batches`, `company_parameters`, `credit_notes`, `customers`, `distribution_codes`, `receivable_types`, `transaction_lines`, `transactions`. |
| `rawFilters[]` | body | `array<object>` | no | Trimble search filters, all combined with AND. Add one item per condition: Property Name, Operator, Value and Value Type (Trimble does not convert types, so use Number for integer properties like Customer and a list type for In). Can be combined with the filter builder. |
| `rawFilters[].value` | body | `string` | no | Value to compare against. For the In operator, pass a comma-separated list (111,10009) or a JSON array ([111,10009]). Set Value Type so it is sent with the JSON type Trimble expects. |
| `rawFilters[].valueType` | body | `list<string>` | no | JSON type Trimble expects for this property (it does not convert types: Customer = "10009" as text matches nothing). Number for integer properties such as Customer, CustGroup, KeyID; Text for text properties such as Name, Status, Zip; Boolean for true/false; Number List / Text List for the In operator. Empty = value is sent as received. Accepted values: `boolean`, `number`, `numberList`, `text`, `textList`. |
