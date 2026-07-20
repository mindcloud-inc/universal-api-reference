# Get Apple OS Version with Tophhie Cloud

Retrieves the latest Apple OS version for a device in Tophhie Cloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/appleosversion/{appleDeviceModel}`
- **Base URL:** `https://api.tophhie.cloud`
- **Official documentation:** [Get Apple OS Version](https://api.tophhie.cloud/swagger/v1/swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appleDeviceModel` | path | `string` | yes | Apple hardware identifier, for example iPhone17,1. |
| `currentOSVersion` | query | `string` | no | Current Apple OS version to compare against. |
