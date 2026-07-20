# Validate API Key with DitLead

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/apikey/validate`
- **Base URL:** `https://api.ditlead.com`
- **Official documentation:** [Validate API Key](https://ditlead.com/developer/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `keyType` | body | `string` | yes | Key classification to validate. DitLead documents `platform` and `system`. Accepted values: `0`, `1`. |
