# Send Multiline Event with Loggly (Send Data)

Creates a multiline log event in Loggly.

## Endpoint

- **Method:** `POST`
- **Path:** `/inputs/:customerToken/tag/:tagPath/`
- **Base URL:** `https://logs-01.loggly.com`
- **Official documentation:** [Send Multiline Event](https://documentation.solarwinds.com/en/success_center/loggly/content/admin/http-endpoint.htm)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customerToken` | path | `string` | yes |
| `tagPath` | path | `string` | yes |
| `message` | body | `string` | yes |
