# Create Workers Comp with Aspire

Creates a new workers comp record in your Aspire account.

## Endpoint

- **Method:** `POST`
- **Path:** `WorkersComps`
- **Base URL:** `https://{environment}.youraspire.com/`
- **Official documentation:** [Create Workers Comp](https://cloud-api.youraspire.com/swagger/index.html#/WorkersComps/WorkersComps_Create)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `WorkersCompName` | body | `string` | yes |
| `WorkersCompCode` | body | `string` | yes |
