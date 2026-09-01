# Update AP Bill Custom Fields with ServiceTitan

## Endpoint

- **Method:** `PATCH`
- **Path:** `accounting/v2/tenant/{tenant}/ap-bills/custom-fields`
- **Base URL:** `https://{baseUrl}/`
- **Official documentation:** [Update AP Bill Custom Fields](https://developer.servicetitan.io/docs/apis/tenant-accounting-v2/endpoints/ApBills_UpdateCustomFields)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `operations[]` | body | `array<object>` | yes | AP bill custom-field update operations. Each item must include objectId and customFields name/value pairs. |
