# Search Devices with Peplink

## Endpoint

- **Method:** `GET`
- **Path:** `devices/search`
- **Base URL:** `https://portal.peplink.com/api/e/v1/cp/`
- **Official documentation:** [Search Devices](https://portal.peplink.com/docs/api-reference/devices/search/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sns` | query | `string` | no | Enter serial numbers of devices to find. Use , as separator for multiple serial numbers. |
