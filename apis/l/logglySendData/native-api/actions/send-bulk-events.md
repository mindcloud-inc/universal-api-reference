# Send Bulk Events with Loggly (Send Data)

Creates bulk log events in Loggly.

## Endpoint

- **Method:** `POST`
- **Path:** `/bulk/:customerToken/tag/:tagPath/`
- **Base URL:** `https://logs-01.loggly.com`
- **Official documentation:** [Send Bulk Events](https://documentation.solarwinds.com/en/success_center/loggly/content/admin/api-sending-data.htm)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerToken` | path | `string` | yes | Loggly customer token used in the ingestion URL path. |
| `tagPath` | path | `string` | yes | One tag or a slash-delimited tag path to attach to all bulk events. |
| `events` | body | `string` | yes | Newline-delimited bulk event payload. |
