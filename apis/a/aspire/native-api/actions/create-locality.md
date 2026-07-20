# Create Locality with Aspire

Creates a new locality in your Aspire account.

## Endpoint

- **Method:** `POST`
- **Path:** `Localities`
- **Base URL:** `https://{environment}.youraspire.com/`
- **Official documentation:** [Create Locality](https://cloud-api.youraspire.com/swagger/index.html#/Localities/Localities_Create)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `LocalityName` | body | `string` | yes |
| `LocalCode` | body | `string` | no |
| `Active` | body | `boolean` | yes |
