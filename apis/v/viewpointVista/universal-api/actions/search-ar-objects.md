# Viewpoint Vista: Search AR Objects

Search objects found in the Viewpoint® Vista™ Accounts Receivable (AR) programs.

```
GET https://connect.mindcloud.co/v1/universal/viewpointVista/latest/actions/search-ar-objects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Viewpoint Vista `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/viewpointVista/latest/actions/search-ar-objects?connectionId=$CONNECTION_ID&object=batch_entries" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "object": "batch_entries"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/viewpointVista/latest/actions/search-ar-objects?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `modifiedUtcAfter` | date | no |  |
| `rawFilters[].propertyName` | string | no | Property of the object to filter on, exactly as Trimble returns it (case-sensitive), e.g. Customer, Name, CustGroup. Dot-notation works for nested properties (e.g. __custom_fields.udServiceTitanId), but not for properties inside arrays. Example: `Customer`. |
| `modifiedUtcBefore` | date | no |  |
| `rawFilters[].operator` | list<string> | no | Comparison operator. Like, StartsWith, EndsWith and Contains work only on text values. In needs a list value. One of: `Contains`, `EndsWith`, `Equal`, `GreaterThan`, `GreaterThanOrEqual`, `In`, `LessThan`, `LessThanOrEqual`, `Like`, `NotEqual`, `StartsWith`. |
| `object` | list<string> | yes | Specify the type of Object from the Accounts Receivable V2 Direct API that you'd like to retrieve. One of: `batch_entries`, `batch_entry_lines`, `batches`, `company_parameters`, `credit_notes`, `customers`, `distribution_codes`, `receivable_types`, `transaction_lines`, `transactions`. |
| `rawFilters[]` | array<object> | no | Trimble search filters, all combined with AND. Add one item per condition: Property Name, Operator, Value and Value Type (Trimble does not convert types, so use Number for integer properties like Customer and a list type for In). Can be combined with the filter builder. Example: `[object Object]`. |
| `rawFilters[].value` | string | no | Value to compare against. For the In operator, pass a comma-separated list (111,10009) or a JSON array ([111,10009]). Set Value Type so it is sent with the JSON type Trimble expects. Example: `10009`. |
| `rawFilters[].valueType` | list<string> | no | JSON type Trimble expects for this property (it does not convert types: Customer = "10009" as text matches nothing). Number for integer properties such as Customer, CustGroup, KeyID; Text for text properties such as Name, Status, Zip; Boolean for true/false; Number List / Text List for the In operator. Empty = value is sent as received. One of: `boolean`, `number`, `numberList`, `text`, `textList`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Viewpoint Vista API returns.

## Native endpoint

Through the native Viewpoint Vista API, this operation is `POST v1/direct/subscribers/:subscriber_code/vista/:api/2/data/:object/cache/search` (base URL `https://api.xchange.trimble.com/connect/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-ar-objects.md) for the provider-specific parameters and requirements.

