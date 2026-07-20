# Search Companies with Finnish BIS

Finds companies in Finnish BIS.

## Endpoint

- **Method:** `GET`
- **Path:** `/companies`
- **Base URL:** `https://avoindata.prh.fi/opendata-ytj-api/v3`
- **Official documentation:** [Search Companies](https://avoindata.prh.fi/opendata-ytj-api/v3/schema?lang=en)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | query | `string` | no | Company name. Searches current, previous, parallel, and auxiliary company names. |
| `location` | query | `string` | no | Town or city. |
| `businessId` | query | `string` | no | Finnish Business ID, for example 0116297-6. |
| `companyForm` | query | `list<string>` | no | Company form code from the PRH YRMU code list. Accepted values: `AOY`, `ASH`, `ASY`, `AY`, `AYH`, `ETS`, `ETY`, `HY`, `KOY`, `KVJ`, `KVY`, `KY`, `OK`, `OP`, `OY`, `OYJ`, `SCE`, `SCP`, `SE`, `SL`, `SP`, `SÄÄ`, `TYH`, `VALTLL`, `VOJ`, `VOY`, `VY`. |
| `mainBusinessLine` | query | `string` | no | Statistics Finland TOL 2008 main business line code or text. |
| `registrationDateStart` | query | `date` | no | Company registration date range start in yyyy-mm-dd format. |
| `registrationDateEnd` | query | `date` | no | Company registration date range end in yyyy-mm-dd format. |
| `postCode` | query | `string` | no | Postal code of street or postal address. Maximum length: 5. |
| `businessIdRegistrationStart` | query | `date` | no | Business ID grant date range start in yyyy-mm-dd format. |
| `businessIdRegistrationEnd` | query | `date` | no | Business ID grant date range end in yyyy-mm-dd format. |
| `page` | query | `number` | no | Results page number. If omitted or out of range, PRH returns the first page. |
