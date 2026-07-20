# Check Conversion Support with ConvertHub

Checks whether ConvertHub supports a specific format conversion.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/formats/:sourceFormat/to/:targetFormat`
- **Base URL:** `https://api.converthub.com/v2`
- **Official documentation:** [Check Conversion Support](https://converthub.com/api/docs)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `sourceFormat` | path | `string` | yes |
| `targetFormat` | path | `string` | yes |
