# Download Transfer Lists with Dachser

Downloads transfer lists for a specific date from Dachser.

## Endpoint

- **Method:** `GET`
- **Path:** `/rest/v2/transferlists/{orderdate}`
- **Base URL:** `https://api-gateway.dachser.com/`
- **Official documentation:** [Download Transfer Lists](https://api-portal.dachser.com/bi.b2b.portal/api/library/transportorder)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderdate` | path | `date` | yes | Transfer list order date. |
| `acceptLanguage` | query | `string` | no | Optional language sent as the Accept-Language header. |
