# Send JSON Event with Loggly (Send Data)

Creates a JSON log event in Loggly.

## Endpoint

- **Method:** `POST`
- **Path:** `/inputs/:customerToken/tag/:tagPath/`
- **Base URL:** `https://logs-01.loggly.com`
- **Official documentation:** [Send JSON Event](https://documentation.solarwinds.com/en/success_center/loggly/content/admin/api-sending-data.htm)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerToken` | path | `string` | yes | Loggly customer token used in the ingestion URL path. |
| `tagPath` | path | `string` | yes | One tag or a slash-delimited tag path to attach to the event. |
| `payload` | body | `object` | yes | JSON object to send as the log event body. |
