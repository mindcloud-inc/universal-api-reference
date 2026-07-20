# Add Offline User Data Job Operations with Google Ads

Adds operations to an offline user data job in Google Ads.

## Endpoint

- **Method:** `POST`
- **Path:** `v22/customers/:customerId/offlineUserDataJobs/:offlineUserDataJobId:addOperations`
- **Base URL:** `https://googleads.googleapis.com/`
- **Official documentation:** [Add Offline User Data Job Operations](https://developers.google.com/google-ads/api/reference/rpc/v22/OfflineUserDataJobService/AddOfflineUserDataJobOperations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `list` | yes | Customer ID that owns the Google Ads resources (without dashes). |
| `offlineUserDataJobId` | path | `string` | yes | Offline user data job ID to append operations to. |
| `operations[]` | body | `array<object>` | yes | Offline user data job operations to add. |
| `validateOnly` | body | `boolean` | no | When true, validates the request without executing mutations. |
