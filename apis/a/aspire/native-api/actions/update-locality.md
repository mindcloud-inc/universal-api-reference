# Update Locality with Aspire

Updates an existing locality in your Aspire account.

## Endpoint

- **Method:** `PUT`
- **Path:** `Localities`
- **Base URL:** `https://{environment}.youraspire.com/`
- **Official documentation:** [Update Locality](https://cloud-api.youraspire.com/swagger/index.html#/Localities/Localities_Update)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `LocalityName` | body | `string` | yes |
| `LocalCode` | body | `string` | no |
| `Active` | body | `boolean` | yes |
| `LocalityID` | body | `number` | yes |
