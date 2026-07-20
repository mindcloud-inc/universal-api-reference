# Lookup DKIM Record with Mx Toolbox

## Endpoint

- **Method:** `GET`
- **Path:** `/lookup/dkim`
- **Base URL:** `https://api.mxtoolbox.com/api/v1`
- **Official documentation:** [Lookup DKIM Record](https://mxtoolbox.com/dkim.aspx)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `argument` | query | `string` | yes | Provide either domain:selector or selector._domainkey.domain. |
