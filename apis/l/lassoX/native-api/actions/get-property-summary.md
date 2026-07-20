# Get Property Summary with Lasso X

Retrieves a property summary from Lasso X.

## Endpoint

- **Method:** `GET`
- **Path:** `/data/bbr/property/summary`
- **Base URL:** `https://api.lassox.com`
- **Official documentation:** [Get Property Summary](https://docs.lassox.com/data-apis/bbr/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `propertynumber` | query | `number` | yes | Property number. |
| `municipality` | query | `number` | yes | Municipality code. |
