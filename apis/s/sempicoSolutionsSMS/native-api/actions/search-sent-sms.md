# Search Sent SMS with Sempico Solutions SMS

## Endpoint

- **Method:** `POST`
- **Path:** `/sms-full-data`
- **Base URL:** `https://restapi.sempico.solutions/v1`
- **Official documentation:** [Search Sent SMS](https://pypi.org/pypi/gatum-rest-py/json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `MCC` | body | `number` | no | Optional mobile country code filter. |
| `MNC` | body | `number` | no | Optional mobile network code filter. |
| `sender` | body | `string` | no | Optional Sender ID filter. |
| `phone[]` | body | `array<string>` | no | Optional phone number filters. |
| `id_base[]` | body | `array<number>` | no | Optional group ID filters. |
| `time_period` | body | `string` | no | Optional SMS sending period filter, for example 2023-07-24 00:00:00 - 2023-07-24 23:59:59. |
| `type_sms` | body | `list` | no | Optional SMS type filter. Sempico documents sms, hlr, and mnp. Accepted values: `0`, `1`, `2`. |
| `limit` | body | `number` | no | Optional number of sent SMS records to return. |
