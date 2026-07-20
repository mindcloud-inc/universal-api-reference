# Upload Log File with Loggly (Send Data)

Uploads a log file to Loggly.

## Endpoint

- **Method:** `POST`
- **Path:** `/bulk/:customerToken/tag/:tagPath/`
- **Base URL:** `https://logs-01.loggly.com`
- **Official documentation:** [Upload Log File](https://documentation.solarwinds.com/en/success_center/loggly/content/admin/file-upload.htm)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerToken` | path | `string` | yes | — |
| `tagPath` | path | `string` | yes | — |
| `file` | body | `file` | yes | Text log file to upload. Each line becomes an event in Loggly. |
