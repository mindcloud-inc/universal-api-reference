# Run MCA Analysis with Docsumo

Retrieves monthly account summary analysis from Docsumo bank statements.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/skitty/analytics/account-summary/`
- **Base URL:** `https://app.docsumo.com`
- **Official documentation:** [Run MCA Analysis](https://support.docsumo.com/reference/mca-analysis)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `run` | body | `string` | yes | Run control value. Use now to calculate analytics immediately. |
