# Create Expenditure with Refrens

## Endpoint

- **Method:** `POST`
- **Path:** `/businesses/:urlKey/expenditures`
- **Base URL:** `https://api.refrens.com`
- **Official documentation:** [Create Expenditure](https://www.refrens.com/api/docs/expenditure/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `billedBy` | body | `object` | yes |
| `items[]` | body | `array<object>` | yes |
| `invoiceDate` | body | `date` | no |
