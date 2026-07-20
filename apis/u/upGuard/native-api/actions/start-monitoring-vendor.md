# Start Monitoring Vendor with UpGuard

Starts monitoring a vendor in UpGuard.

## Endpoint

- **Method:** `POST`
- **Path:** `/vendor/monitor`
- **Base URL:** `https://cyber-risk.upguard.com/api/public`
- **Official documentation:** [Start Monitoring Vendor](https://cyber-risk.upguard.com/api/docs#operation/monitorvendor)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `number` | no | The numeric ID of the vendor to begin monitoring. |
| `hostname` | query | `string` | no | The hostname of the vendor to begin monitoring when no vendor ID is provided. |
| `labels[]` | query | `array<string>` | no | Labels to assign to the vendor when monitoring starts. Send multiple values as a string separated by `,`. |
| `tier` | query | `number` | no | Tier to assign to the vendor. |
| `wait_for_scan` | query | `boolean` | no | Wait for scan results on new unknown vendors before returning. |
