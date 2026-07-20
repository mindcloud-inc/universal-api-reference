# Record Conversion with jo4.io

## Endpoint

- **Method:** `POST`
- **Path:** `/protected/url/:slug/conversions`
- **Base URL:** `https://jo4-api.jo4.io/api/v1`
- **Official documentation:** [Record Conversion](https://jo4-api.jo4.io/swagger-ui/index.html#/conversion-controller/recordConversion_1)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `currency` | body | `string` | no |
| `eventType` | body | `string` | no |
| `externalId` | body | `string` | no |
| `metadata` | body | `string` | no |
| `quantity` | body | `number` | no |
| `slug` | path | `string` | yes |
| `value` | body | `number` | no |
