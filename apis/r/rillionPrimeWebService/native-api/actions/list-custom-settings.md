# List Custom Settings with Rillion Prime Web Service

List custom settings in Rillion Prime. Administrative operation.

## Endpoint

- **Method:** `POST`
- **Base URL:** `{baseUrl}`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sCompany` | body | `list<string>` | no | Company to filter by. |
| `sType` | body | `string` | no | Setting type to filter by. |
| `sSetting` | body | `string` | no | Setting name to filter by. |
| `sValue` | body | `string` | no | Setting value to filter by. |
| `CompanyIsNull` | body | `boolean` | no | When true, only return settings that have no company. |
