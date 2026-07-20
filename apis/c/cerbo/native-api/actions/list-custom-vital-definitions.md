# List Custom Vital Definitions with Cerbo

Retrieves custom vital definitions from Cerbo.

## Endpoint

- **Method:** `GET`
- **Path:** `/vitals`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [List Custom Vital Definitions](https://docs.cer.bo/#tag/Vitals/operation/getVitals)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `show_all` | query | `boolean` | no | If set to “true”, returns the entire custom vitals list, otherwise only returns the items configured to appear on patient charts |
