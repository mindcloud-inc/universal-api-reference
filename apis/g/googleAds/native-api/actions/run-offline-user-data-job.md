# Run Offline User Data Job with Google Ads

Runs an offline user data job in Google Ads.

## Endpoint

- **Method:** `POST`
- **Path:** `v22/customers/:customerId/offlineUserDataJobs/:offlineUserDataJobId:run`
- **Base URL:** `https://googleads.googleapis.com/`
- **Official documentation:** [Run Offline User Data Job](https://developers.google.com/google-ads/api/reference/rpc/v22/OfflineUserDataJobService/RunOfflineUserDataJob)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `list` | yes | Customer ID that owns the Google Ads resources (without dashes). |
| `offlineUserDataJobId` | path | `string` | yes | Offline user data job ID to run. |
| `validateOnly` | body | `boolean` | no | When true, validates the request without executing mutations. |
