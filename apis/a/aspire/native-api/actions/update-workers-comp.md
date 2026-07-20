# Update Workers Comp with Aspire

Updates an existing workers comp record in your Aspire account.

## Endpoint

- **Method:** `PUT`
- **Path:** `WorkersComps`
- **Base URL:** `https://{environment}.youraspire.com/`
- **Official documentation:** [Update Workers Comp](https://cloud-api.youraspire.com/swagger/index.html#/WorkersComps/WorkersComps_Update)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `WorkersCompName` | body | `string` | yes |
| `WorkersCompCode` | body | `string` | yes |
| `WorkersCompID` | body | `number` | yes |
